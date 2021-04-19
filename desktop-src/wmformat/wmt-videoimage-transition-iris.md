---
title: 'WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl) '
description: 鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。 此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983100"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 鳶尾花

鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。 此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。

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
<td>相對於影片框架的 X 座標，鳶尾花效果的中心。</td>
</tr>
<tr class="even">
<td>中心 Y</td>
<td><strong>fEffectPara1</strong></td>
<td>相對於影片框架的 Y 座標，鳶尾花效果的中心。</td>
</tr>
<tr class="odd">
<td>寬度</td>
<td><strong>fEffectPara2</strong></td>
<td>垂直線的寬度，以圖元為單位顯示新影像。</td>
</tr>
<tr class="even">
<td>高度</td>
<td><strong>fEffectPara3</strong></td>
<td>水平線的高度會顯示新影像（以圖元為單位）。</td>
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

 

 





