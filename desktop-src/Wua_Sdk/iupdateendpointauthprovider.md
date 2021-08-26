---
description: 包含用來協商用來驗證服務端點的權杖類型的方法。
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: 'IUpdateEndpointAuthProvider 介面 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 3cbc51ab0f1192e20612829532b907e3644a7da3f99fdedd8e3dbd45a780c54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994568"
---
# <a name="iupdateendpointauthprovider-interface"></a>IUpdateEndpointAuthProvider 介面

**IUpdateEndpointAuthProvider** 介面包含用來協商用來驗證服務端點的權杖類型的方法。

## <a name="members"></a>成員

**IUpdateEndpointAuthProvider** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IUpdateEndpointAuthProvider** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUpdateEndpointAuthProvider** 介面具有這些方法。



| 方法                                                                                             | 描述                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | 使用指定的認證，要求服務端點的權杖。<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | 傳回服務端點的慣用驗證 token 類型。<br/> |



 

## <a name="remarks"></a>備註

WUA 會呼叫這個介面的 [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) 方法，以啟動協調進程。 當進行呼叫時，會將服務識別碼、服務所執行的端點類型，以及可用的權杖類型傳遞給 WUA。 然後，此介面的執行會傳回它所 preferes 要使用的權杖類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>                |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>UpdateEndpointAuth .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
