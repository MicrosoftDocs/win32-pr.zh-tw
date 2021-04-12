---
description: 指定管線是否修剪範例。
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: 'MF_TOPOLOGY_NO_MARKIN_MARKOUT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191882"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT 屬性

指定管線是否修剪範例。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

根據預設，管線會修剪範例以符合正確的呈現時間。 修剪是在具有 [**mf \_ TOPONODE \_ MARKIN \_**](mf-toponode-markin-here-attribute.md) 的拓撲節點和 [**mf \_ TOPONODE \_ MARKOUT \_ 這裡**](mf-toponode-markout-here-attribute.md) 的屬性上完成。 如果拓撲上的 [ **MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT** ] 屬性設定為 **TRUE** ，管線不會修剪範例，且會忽略 **此處的 mf \_ TOPONODE \_ MARKIN \_** 和 **mf \_ TOPONODE \_ MARKOUT \_ 這裡** 的屬性。 如果屬性未設定，或值 **為 FALSE**，則管線會修剪範例。

如果應用程式從管線接收壓縮的範例，且需要取得所有的主要畫面格，則應用程式可能會將 [ **MF \_ 拓撲 \_ NO \_ MARKIN \_ MARKOUT** ] 屬性設定為 [ **TRUE** ]，否則可能會被修剪。

這個屬性的預設值為 **FALSE**。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKIN \_ 這裡**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ 這裡**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




