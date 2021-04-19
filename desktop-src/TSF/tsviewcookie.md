---
title: 'TsViewCookie (Textstor) '
description: TsViewCookie 資料類型會識別內容視圖。
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106994974"
---
# <a name="tsviewcookie"></a>TsViewCookie

**TsViewCookie** 資料類型會識別內容視圖。


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>備註

應用程式必須為其所建立的每個視圖提供唯一的 **TsViewCookie** 值。

TSF 管理員會藉由呼叫 [ITextStoreACP：： GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) 或 [ITextStoreAnchor：： GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)，從應用程式取得這個值。 TSF 管理員會在呼叫各種 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 或 [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) 方法時，使用這個值來識別此視圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP：： GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**ITextStoreAnchor::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





