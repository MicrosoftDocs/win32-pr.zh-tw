---
description: 傳回服務端點的慣用驗證 token 類型。
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider：： GetPreferredEndpointTokenType 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191477"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>IUpdateEndpointAuthProvider：： GetPreferredEndpointTokenType 方法

傳回服務端點的慣用驗證 token 類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*serviceId* \[在\]
</dt> <dd>

識別要更新的服務。

</dd> <dt>

*endpointType* \[在\]
</dt> <dd>

識別要連接到服務的端點 tneeded 型別。

</dd> <dt>

*ulRequestedTypes* \[在\]
</dt> <dd>

識別端點所支援的一組 Or 運算 token。

</dd> <dt>

*pulPreferredTokenTypes* \[擴展\]
</dt> <dd>

指定慣用之驗證 token 類型的 Or 運算集。  (設定為0，表示不需要驗證權杖) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 否則，會傳回 COM 或 Windows 錯誤碼。

## <a name="remarks"></a>備註

當傳回此方法時，WUA 會從慣用的類型中選擇 token 類型，並將它傳遞至 [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) 方法的 tokenType 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>                |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>UpdateEndpointAuth .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




