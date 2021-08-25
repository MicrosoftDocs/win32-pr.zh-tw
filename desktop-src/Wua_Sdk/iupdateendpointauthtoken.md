---
description: 提供 WUA 可用來收集端點 token 相關資訊的方法。
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: 'IUpdateEndpointAuthToken 介面 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855758"
---
# <a name="iupdateendpointauthtoken-interface"></a>IUpdateEndpointAuthToken 介面

提供 WUA 可用來收集端點 token 相關資訊的方法。

## <a name="members"></a>成員

**IUpdateEndpointAuthToken** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IUpdateEndpointAuthToken** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUpdateEndpointAuthToken** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | 取得要驗證之服務的識別碼。<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | 取得用來在用戶端電腦與 sercvice 之間簽署外寄訊息的金鑰。<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | 取得 XML 資料 (透過網路) 傳送，以代表權杖。 <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | 取得 token 之附加參考的 XML 格式。<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | 取得標記之未附加參考的 XML 格式。<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | 取得端點 token 的型別，例如 WS-Security SAML (安全性聲明標記語言) 1.1 token。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>                |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>UpdateEndpointAuth .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
