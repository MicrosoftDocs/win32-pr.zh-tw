---
description: 使用指定的認證，要求服務端點的權杖。
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider：： GetEndpointToken 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690716"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>IUpdateEndpointAuthProvider：： GetEndpointToken 方法

使用指定的認證，要求服務端點的權杖。

## <a name="syntax"></a>語法


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
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

識別服務所執行之端點的類型。

</dd> <dt>

*proxySettings* \[在\]
</dt> <dd>

連接至 proxy 伺服器時所要使用的設定。 如需詳細資訊，請參閱 [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) 結構。

</dd> <dt>

*hUserToken* \[在\]
</dt> <dd></dd> <dt>

*tokenType* \[在\]
</dt> <dd>

識別用於驗證的驗證權杖類型。

</dd> <dt>

*fRefreshOnline* \[在\]
</dt> <dd>

表示氣象 WUA 要求新的權杖。 True 表示要求新的權杖。 False 表示要求新的或快取的標記。 如需詳細資訊，請參閱「備註」。

</dd> <dt>

*ppEndpointToken* \[擴展\]
</dt> <dd>

指定要使用的端點權杖。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 否則，會傳回 COM 或 Windows 錯誤碼。

## <a name="remarks"></a>備註

WUA 通常會在第一次呼叫此方法時，將 fRefreshOnline 參數設定為 false，然後如果連接錯誤時 WUA，則會在再次呼叫方法時將該參數設定為 true。 不過，此方法的執行可以從安全性權杖服務 (STS) 要求新的權杖，或隨時提供快取的權杖。

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
</dt> </dl>

 

 




