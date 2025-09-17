section .data
  name db "Artemy Vanchugov", 0xA
  music db "According to my mood", 0xA
  telegram db "https://t.me/makeddonov", 0xA
  msg db "Someone in the world is having fun, someone is feeling good. Everyone`s had some luck in life - but I was lucky."
  message_len equ $ - msg

section .text
  global _start

_start:
  mov rax, 1
  mov rdi, 1
  mov rsi, msg
  mov rdx, message_len
  syscall

_end:
  mov rax, 60
  syscall
