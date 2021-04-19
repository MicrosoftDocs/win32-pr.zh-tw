---
title: 'WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl) '
description: 投影片轉換會將舊影像從框架滑出，以顯示新的影像。
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992907"
---
# <a name="wmt_videoimage_transition_slide"></a>WMT \_ VIDEOIMAGE \_ 轉換投影 \_ 片

投影片轉換會將舊影像從框架滑出，以顯示新的影像。

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
<td>距離</td>
<td><strong>fEffectPara0</strong></td>
<td>舊影像滑出框架的距離（以圖元為單位）。</td>
</tr>
<tr class="even">
<td>方向</td>
<td><strong>fEffectPara1</strong></td>
<td>舊影像滑出的方向。設定為下列其中一個值：<br/>
<ul>
<li>0-滑到右邊。</li>
<li>1-滑至左方。</li>
<li>2-向上滑。</li>
<li>3-向下滑動。</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composition</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





