---
description: 包含媒體來源慣用的 RFC 1766 語言。
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: 'MF_PD_PREFERRED_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd01a47002bf3cd9419579786ff37df1fc03af940f54b2d2a2bb859d5b97007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740709"
---
# <a name="mf_pd_preferred_language-attribute"></a>MF \_ PD \_ 慣用 \_ 語言屬性

包含媒體來源慣用的 RFC 1766 語言。

## <a name="data-type"></a>資料類型

**WCHAR**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="applies-to"></a>適用於

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>備註

[MF \_ PD \_ 慣用 \_ 語言] 屬性是選擇性的。 應用程式可以在媒體來源 (（例如網路來源) ）上設定此屬性，以指定其慣用語言。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




