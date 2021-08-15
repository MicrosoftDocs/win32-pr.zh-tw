---
title: 'WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl) '
description: 「顯示」轉換會顯示來自框架某一端之直線的新影像。
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916a5142f09628852a016754f9fb3ad691882731466d802b8367e03837b9699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083732"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 顯示

「顯示」轉換會顯示來自框架某一端之直線的新影像。

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
<td>顯示的新影像數量（以圖元為單位）。 此值相對於框架的原始端。</td>
</tr>
<tr class="even">
<td>方向</td>
<td><strong>fEffectPara1</strong></td>
<td>洩漏的方向。設定為下列其中一個值：<br/>
<ul>
<li>0-向右顯示;源自框架的左邊。</li>
<li>1-向左顯示;源自框架的右側。</li>
<li>2-向上顯示;源自框架的底部。</li>
<li>3-向下顯示;源自框架的頂端。</li>
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

 

 





