---
description: 下列 Guid 會定義媒體基礎轉換 (MFTs) 的分類。 這些類別用來註冊和列舉 MFTs。
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: 'MFT_CATEGORY (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848714"
---
# <a name="mft_category"></a>MFT \_ 類別

下列 Guid 會定義媒體基礎轉換 (MFTs) 的分類。 這些類別用來註冊和列舉 MFTs。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">音訊解碼器。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">音訊效果。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">音訊編碼器。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Demultiplexers.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Multiplexers.<br/>
<blockquote>
[!Note]<br />
在 Windows Vista 中，媒體基礎管線不支援具有多個輸入的 MFTs。 Windows 7 支援多重輸入 MFTs。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <dt><strong>MFT_CATEGORY_OTHER</strong></dt> </dl></td>
<td style="text-align: left;">其他 MFTs。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">影片解碼器。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">影片效果。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">影片轉譯器效果。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">影片編碼器。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
在 Windows 7 中引進。
</blockquote>
<br/> 影片處理器。 <br/> 此類別僅限於在未壓縮的影片上執行格式轉換的 MFTs，包括色彩空間轉換。 針對修改影像外觀的影片效果 (例如模糊效果或彩色到灰階的轉換) ，請使用 <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> 類別目錄。<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




