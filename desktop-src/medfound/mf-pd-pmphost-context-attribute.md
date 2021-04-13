---
description: 包含應用程式呈現描述項之 proxy 物件的指標。
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: 'MF_PD_PMPHOST_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386247"
---
# <a name="mf_pd_pmphost_context-attribute"></a>MF \_ PD \_ PMPHOST \_ 內容屬性

包含應用程式之展示描述項的 proxy 物件指標。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

受保護的媒體路徑 (PMP) 主機會使用這個屬性，將應用程式的呈現描述項儲存在遠端呈現描述項上。 屬性值是 [_ *IMFRemoteProxy* *](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)介面的指標。

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




