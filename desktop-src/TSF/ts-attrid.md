---
title: 'TS_ATTRID (Textstor) '
description: TS \_ ATTRID 資料類型是用來識別文字屬性。
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1c40d56f1f8ff3deb59d0dd7664a197a672ade7b2d53beebd8e35ba5de7c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950334"
---
# <a name="ts_attrid"></a>TS \_ ATTRID

**TS \_ ATTRID** 資料類型是用來識別文字屬性。


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>備註

預先定義的 TS ATTRID Guid 清單 \_ 位於 tsattrs。

Guid TSATTRID \_ 文字 \_ VERTICALWRITING 和 TSATTRID \_ 文字方向適用于 \_ 應用程式，以符合要更正的輸入文字。 您可以建立其他使用者定義的 Guid。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITextStoreACP：： FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP：： RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP：： RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP：： RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink：： OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**ITextStoreAnchor::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**ITextStoreAnchorSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**TS \_ ATTRVAL**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





