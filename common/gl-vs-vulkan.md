# OpenGL vs Vulkan

Currently, there are two graphic APIs commonly used on Linux - OpenGL and Vulkan. Some applications support both and allow to choose which one to use. This article covers which one should you use depending on your video card.

## Nvidia - OpenGL preferred

In general, Nvidia have very good OpenGL support on Linux, while Vulkan is comparably weak. Unless using Vulkan carries some benefits other than performance, OpenGL is the way to go

## AMD - Vulkan preferred

In AMD's case, Vulkan tends to have better performance if it's done well application-side, with OpenGL being worse. There is a good chance that giving Vulkan a go on AMD is a good idea.

## Intel - Vulkan preferred (?)

It seems that Intel prefers a little better on Vulkan, but there probably isn't too much of a difference. Try out what works out better for your application.
