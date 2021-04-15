---
description: 指定應用程式所控制 (LTR) 框架的最大長期參考數目。
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: 'CODECAPI_AVEncVideoLTRBufferControl 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510819"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>CODECAPI \_ AVEncVideoLTRBufferControl 屬性

指定應用程式所控制 (LTR) 框架的最大長期參考數目。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>屬性值

此控制項的值包含兩個欄位，其中每個欄位都有16個位。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>第一個欄位</strong></dt><dt>位 [0.. 15]</dt> </dl></td>
<td>應用程式所控制的 LTR 框架數目。<br/> <strong>H.264/AVC 編碼器：</strong><br/> 假設值為 N 而 N 為非零值，則在每個 IDR 的畫面上，編碼器必須自動將 IDR 框架之後的框架標示 (，並將 IDR 框架) 為 LTR 框架，只要下列全部3項適用：
<ul>
<li>框架尚未設定為標示為長期參考框架。</li>
<li>框架是基底圖層框架。 例如，語法元素 <strong>temporal_id</strong> 等於0。</li>
<li>目前標示為 LTR 的框架數目小於 N。</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>第二個欄位</strong></dt><dt>位 [16.. 31]</dt> </dl></td>
<td>LTR 控制項的信任模式。<br/> <strong>H.264/AVC 編碼器：</strong><br/> 1 (信任直到) 表示編碼器可能會使用 LTR 框架，除非應用程式透過 <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> 控制項明確使其失效。 <br/> 其他值是不正確，並保留供日後使用。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

這是靜態 API。

預設值應為0

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




