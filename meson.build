project('use-hello-gen', 'c')

genhello = find_program(
  'genhello',
  fallback: ['stuff', 'genhello'],
  required: true,
)
gen = custom_target(
  'greeter',
  command: [genhello, 'luke', 'hello.c'],
  output: 'hello.c',
)
hello = executable('hello', gen)
