---
title: 'WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl) '
description: 內凹轉換會在源自框架某一個角落的矩形中顯示新影像。
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987066"
---
# <a name="wmt_videoimage_transition_inset"></a>WMT \_ VIDEOIMAGE \_ 轉換內 \_ 凹

內凹轉換會在源自框架某一個角落的矩形中顯示新影像。

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
<td>寬度</td>
<td><strong>fEffectPara0</strong></td>
<td>內凹的寬度（以圖元為單位）。</td>
</tr>
<tr class="even">
<td>高度</td>
<td><strong>fEffectPara1</strong></td>
<td>內凹的高度（以圖元為單位）。</td>
</tr>
<tr class="odd">
<td>方向</td>
<td><strong>fEffectPara2</strong></td>
<td>內凹來源的邊角。設定為下列其中一個值：<br/>
<ul>
<li>0-左下角</li>
<li>1-右下</li>
<li>2-左上</li>
<li>3-右上</li>
</ul></td>
</tr>
<tr class="even">
<td>Composition</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





