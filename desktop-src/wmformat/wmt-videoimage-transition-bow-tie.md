---
title: 'WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl) '
description: 凸起系結轉換會將新影像顯示在框架的相反邊的一組三角形中。
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992383"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 凸起 \_ 系結

凸起系結轉換會將新影像顯示在框架的相反邊的一組三角形中。

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
<td>凸起系結之每個三角形側的寬度。</td>
</tr>
<tr class="even">
<td>高度</td>
<td><strong>fEffectPara1</strong></td>
<td>凸起系結的每個三角形的高度。</td>
</tr>
<tr class="odd">
<td>方向</td>
<td><strong>fEffectPara2</strong></td>
<td>設定為下列其中一個值：
<ul>
<li>0-指定水準凸起系結效果，其中三角形會從框架的右邊和左邊輸入。</li>
<li>1-指定垂直凸起系結效果，其中三角形會從框架的頂端和底部進入。</li>
</ul></td>
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

 

 





