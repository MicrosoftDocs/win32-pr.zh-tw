---
description: 包含從受保護媒體路徑到展示描述項的指標 (PMP) 。
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: 'MF_PD_APP_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194285"
---
# <a name="mf_pd_app_context-attribute"></a>MF \_ PD \_ 應用程式 \_ 內容屬性

包含從受保護媒體路徑到展示描述項的指標 (PMP) 。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

在 PMP 程式中建立的媒體來源 proxy 會使用這個屬性，將遠端表示描述項儲存在應用程式的呈現描述項上。

這個屬性的值是 [_ *IMFPresentationDescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)介面的指標。

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

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




