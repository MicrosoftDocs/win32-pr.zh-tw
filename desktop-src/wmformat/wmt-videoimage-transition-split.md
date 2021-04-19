---
title: 'WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl) '
description: 分割轉換會藉由分割舊影像來顯示新的影像。 分割會沿著框架內的水準水準或垂直線出現。
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981353"
---
# <a name="wmt_videoimage_transition_split"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 分割

分割轉換會藉由分割舊影像來顯示新的影像。 分割會沿著框架內的水準水準或垂直線出現。

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
<td>分割之原始線的相對於影片框架的 X 座標。</td>
</tr>
<tr class="even">
<td>中心 Y</td>
<td><strong>fEffectPara1</strong></td>
<td>相對於影片框架的 Y 座標（相對於影片框架）。</td>
</tr>
<tr class="odd">
<td>距離</td>
<td><strong>fEffectPara2</strong></td>
<td>分割的寬度（以圖元為單位）。</td>
</tr>
<tr class="even">
<td>方向</td>
<td><strong>fEffectPara3</strong></td>
<td>分割的方向。設定為下列其中一個值：<br/>
<ul>
<li>0-沿著水平線分割。</li>
<li>1-沿著垂直線分割。</li>
</ul></td>
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

 

 





