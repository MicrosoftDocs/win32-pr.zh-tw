---
title: 'WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl) '
description: 星形轉換會以框架內的五個指向星形顯示新影像。
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd5a00c7cf68feea13dc0e617e5fe2adb34551032c8ec54bda6e0810fbb092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195168"
---
# <a name="wmt_videoimage_transition_star"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 星星

星形轉換會以框架內的五個指向星形顯示新影像。

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
<td>星形中間的 X 座標（相對於影片框架）。</td>
</tr>
<tr class="even">
<td>中心 Y</td>
<td><strong>fEffectPara1</strong></td>
<td>星形中央的 Y 座標（相對於影片框架）。</td>
</tr>
<tr class="odd">
<td>半徑</td>
<td><strong>fEffectPara2</strong></td>
<td>星形點所定義之圓形的半徑（以圖元為單位）。</td>
</tr>
<tr class="even">
<td>Composition</td>
<td><strong>fEffectPara3</strong></td>
<td>設定為下列其中一個值：
<ul>
<li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li>
<li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景。</li>
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

 

 





