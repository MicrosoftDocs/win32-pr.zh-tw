---
title: 'WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl) '
description: 菱形轉換會顯示菱形中的新影像。
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e3abfa337edd58fc536e530eb0ff6473c9a9d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999104"
---
# <a name="wmt_videoimage_transition_diamond"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 鑽石

菱形轉換會顯示菱形中的新影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>結構成員</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>中心 X</td>
<td><strong>fEffectPara0</strong></td>
<td>相對於影片框架的 X 座標（相對於菱形的中心）。</td>
</tr>
<tr class="even">
<td>中心 Y</td>
<td><strong>fEffectPara1</strong></td>
<td>相對於菱形中間的影片框架的 Y 座標。</td>
</tr>
<tr class="odd">
<td>寬度</td>
<td><strong>fEffectPara2</strong></td>
<td>鑽石的寬度（以圖元為單位）。</td>
</tr>
<tr class="even">
<td>高度</td>
<td><strong>fEffectPara3</strong></td>
<td>鑽石的高度（以圖元為單位）。</td>
</tr>
<tr class="odd">
<td>Composition</td>
<td><strong>fEffectPara4</strong></td>
<td>設定為下列其中一個值：
<ul>
<li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li>
<li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





