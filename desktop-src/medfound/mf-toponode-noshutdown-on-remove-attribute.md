---
description: 指定媒體會話如何關閉拓撲中的物件。
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: 'MF_TOPONODE_NOSHUTDOWN_ON_REMOVE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993000"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>\_ \_ \_ 移除屬性上的 MF TOPONODE NOSHUTDOWN \_

指定媒體會話如何關閉拓撲中的物件。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會套用至下列類型的拓撲節點：

-   輸出節點
-   任何包含 *非同步* 媒體基礎轉換 (MFT) 的轉換節點。

屬性可以具有下列值：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>當媒體會話切換至新拓撲或清除目前的拓撲時，不會關閉屬於此拓撲節點的物件。</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>當媒體會話切換至新拓撲或清除目前的拓撲時，它會關閉節點物件，如下所示：
<ul>
<li>輸出節點：會話會呼叫媒體接收器上的 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink：： Shutdown</strong></a> 。</li>
<li>轉換節點：會話會呼叫 MFT 上的 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown：： Shutdown</strong></a> 。</li>
</ul></td>
</tr>
</tbody>
</table>



 

預設值為 **TRUE**。

如果您的應用程式將多個拓撲排入佇列，最好將此屬性設定為 **FALSE**。 否則，拓撲中的物件可能無法正確地關閉。

當應用程式透過呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)關閉媒體會話時，不會套用此屬性。 當媒體會話關閉時，它一律會關閉目前拓撲中的媒體接收器和非同步 MFTs。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




