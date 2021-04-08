---
description: 包含 Microsoft 媒體基礎 HTTP 位元組資料流程的 IMFNetResourceFilter 回呼介面指標。
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: 'MFNETSOURCE_RESOURCE_FILTER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691807"
---
# <a name="mfnetsource_resource_filter-property"></a>MFNETSOURCE \_ 資源 \_ 篩選屬性

包含 Microsoft 媒體基礎 HTTP 位元組資料流程的 [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) 回呼介面指標。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown \** _

VT \_ 不明

_ *punkVal**



## <a name="remarks"></a>備註

您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。 若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
