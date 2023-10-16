<!--Copyright 2023 The HuggingFace Team. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with
the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on
an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
-->

# ImageBind

## Overview

The ImageBind model was proposed in [ImageBind: One Embedding Space To Bind Them All](https://arxiv.org/abs/2305.05665) by Rohit Girdhar, Alaaeldin El-Nouby, Zhuang Liu, Mannat Singh, Kalyan Vasudev Alwala, Armand Joulin, Ishan Misra.
ImageBind is a multimodal joint embedding model for image/video, text, audio, depth, IMU, and thermal images.
For any input from these six modalities, it outputs the same-sized embedding that can be used for cross-modal and multimodal tasks.

The abstract from the paper is the following:

*We present ImageBind, an approach to learn a joint embedding across six different modalities - images, text, audio, depth, thermal, and IMU data. We show that all combinations of paired data are not necessary to train such a joint embedding, and only image-paired data is sufficient to bind the modalities together. ImageBind can leverage recent large scale vision-language models, and extends their zero-shot capabilities to new modalities just by using their natural pairing with images. It enables novel emergent applications 'out-of-the-box' including cross-modal retrieval, composing modalities with arithmetic, cross-modal detection and generation. The emergent capabilities improve with the strength of the image encoder and we set a new state-of-the-art on emergent zero-shot recognition tasks across modalities, outperforming specialist supervised models. Finally, we show strong few-shot recognition results outperforming prior work, and that ImageBind serves as a new way to evaluate vision models for visual and non-visual tasks.*

Tips:

<INSERT TIPS ABOUT MODEL HERE>

This model was contributed by [dg845](https://huggingface.co/dg845) and [shehan97](https://huggingface.co/shehan97).
The original code can be found [here](https://github.com/facebookresearch/ImageBind).


## ImageBindConfig

[[autodoc]] ImageBindConfig
    - from_text_vision_configs

## ImageBindTextConfig

[[autodoc]] ImageBindTextConfig

## ImageBindVisionConfig

[[autodoc]] ImageBindVisionConfig

## ImageBindTokenizer

[[autodoc]] ImageBindTokenizer
    - build_inputs_with_special_tokens
    - get_special_tokens_mask
    - create_token_type_ids_from_sequences
    - save_vocabulary

## ImageBindTokenizerFast

[[autodoc]] ImageBindTokenizerFast

## ImageBindImageProcessor

[[autodoc]] ImageBindImageProcessor
    - preprocess

## ImageBindFeatureExtractor

[[autodoc]] ImageBindFeatureExtractor

## ImageBindProcessor

[[autodoc]] ImageBindProcessor

## ImageBindModel

[[autodoc]] ImageBindModel
    - forward
    - get_text_features
    - get_image_features

## ImageBindTextModel

[[autodoc]] ImageBindTextModel
    - forward

## ImageBindTextModelWithProjection

[[autodoc]] ImageBindTextModelWithProjection
    - forward

## ImageBindVisionModelWithProjection

[[autodoc]] ImageBindVisionModelWithProjection
    - forward


## ImageBindVisionModel

[[autodoc]] ImageBindVisionModel
    - forward