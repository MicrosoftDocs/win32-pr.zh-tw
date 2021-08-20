---
description: 定義可用來向端點驗證的標記類型。
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: 'UpdateEndpointAuthTokenType 列舉 (UpdateEndpointAuth) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: b9e3efbff48097dcede12d5c8d3117171ef622f20a3bf017b12c6d3ce13a1c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814710"
---
# <a name="updateendpointauthtokentype-enumeration"></a>UpdateEndpointAuthTokenType 列舉

定義可用來向端點驗證的標記類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**
</dt> <dd>

不需要驗證權杖。

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

端點的驗證權杖是 WS-Security 的 SAML (安全性聲明標記語言) 1.1 權杖。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |



 

 




