---
description: 包含媒體來源之展示描述項的指標。
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: 'MF_TOPONODE_PRESENTATION_DESCRIPTOR 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691256"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>MF \_ TOPONODE \_ 展示 \_ 描述項屬性

包含媒體來源之展示描述項的指標。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

此屬性適用于 (_ * MF \_ 拓撲 \_ SOURCESTREAM \_ 節點 * * ) 的來源節點。

屬性的值是標記法描述項的 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。 這是必要屬性。

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 




