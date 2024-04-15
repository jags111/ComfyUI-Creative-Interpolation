# Steerable Motion, a ComfyUI custom node for steering videos with batches of images

Steerable Motion is a ComfyUI node for batch creative interpolation. Our goal is to feature the best quality and most precise and powerful methods for steering motion with images as video models evolve.	This node is best used via [Dough](https://github.com/banodoco/dough) - a creative tool which simplifies the settings and provides a nice creative flow - or in Discord - by joining this channel.

![Main example](https://github.com/banodoco/steerable-motion/blob/main/demo/main_example.gif)

## Installation in Comfy

1. If you haven't already, install [ComfyUI](https://github.com/comfyanonymous/ComfyUI) and [Comfy Manager](https://github.com/ltdrdata/ComfyUI-Manager) - you can find instructions on their pages.
2. Download [this workflow](https://raw.githubusercontent.com/banodoco/steerable-motion/main/demo/creative_interpolation_example.json) and drop it into ComfyUI.
3. When the workflow opens, download the dependent nodes by pressing "Install Missing Custom Nodes" in Comfy Manager. Search and download the required models from Comfy Manager also - make sure that the models you download have the same name as the ones in the workflow - or you're confident that they're the same.

## Usage

The main settings are:

- Key frame position: how many frames to generate between each main key frame you provide.
- Length of influence: what range of frames to apply the IP-Adapter (IPA) influence to.
- Strength of influence: what the low-point and high-point of each frame should be.
- Image adherence: how much we should force adherence to the input images.

Other than image adherence which is set for the entire generation these are set linearly - the same for each frame - or dynamically - varying them for each frame - you can find detailed instructions on how to tweak these settings inside the workflow above.

Tweaking the settings can greatly influence the motion - for example, below you can see two examples of the same images animated - but with the one setting tweaked, the length of each frame's influence:

![Tweaking settings example](https://github.com/banodoco/steerable-motion/blob/main/demo/tweaking_settings.gif)

## Philosophy for getting the most from this

This isn’t a tool like text to video that will perform well out of the box, it’s more like a paint brush - an artistic tool that you need to figure out how to get the best from. 

Through trial and error, you'll need to build an understanding of how the motion and settings work, what its limitations are, which inputs images work best with it, etc.

It won't work for everything but if you can figure out how to wield it, this approach can provide enough control for you to make beautiful things that match your imagination precisely.

## Want to help explore new ways to use this and expand the capabilities?

I believe that that are endless ways to expand upon and extend the ideas in this node.

In an example included in the workflow, you can use [Ostris' Composition IPA](https://huggingface.co/ostris/ip-composition-adapter) to provide  structure to the generation:

![IPA Structure](https://github.com/banodoco/steerable-motion/blob/main/demo/ipa_structure.gif)

Additionally, in [this example by Superbeasts.ai](https://raw.githubusercontent.com/banodoco/steerable-motion/main/demo/SuperBeasts-POM-SmoothBatchCreative-V1.3.json), you can see how he uses depth maps to control the motion in different layers to create a smoother motion effect. There are endless possibilities!


## Want to give feedback, or join a community who are pushing open source models to their artistic and technical limits?

You're very welcome to drop into our Discord [here](https://discord.com/invite/8Wx9dFu5tP).

## Credits

This code draws heavily from Cubiq's [IPAdapter_plus](https://github.com/cubiq/ComfyUI_IPAdapter_plus), while the workflow uses Kosinkadink's [Animatediff Evolved](https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved) and [ComfyUI-Advanced-ControlNet](https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet), Fizzledorf's [Fizznodes](https://github.com/FizzleDorf/ComfyUI_FizzNodes), Fannovel16's [Frame Interpolation](https://github.com/Fannovel16/ComfyUI-Frame-Interpolation) and more. Thanks to all and of course the Animatediff team, Controlnet, others, and of course our supportive community!

