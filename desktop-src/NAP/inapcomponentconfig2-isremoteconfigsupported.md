---
title: 'INapComponentConfig2 IsRemoteConfigSupported 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv) 所執行，指出是否支援遠端設定。
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- IsRemoteConfigSupported 方法 NAP
- IsRemoteConfigSupported 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，IsRemoteConfigSupported 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934171"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2：： IsRemoteConfigSupported 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**IsRemoteConfigSupported** 方法是由系統健康狀態驗證 (shv) 來指出是否支援遠端設定。

## <a name="syntax"></a>語法


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*isSupported* \[擴展\]
</dt> <dd>

如果元件支援遠端設定，則為布林 **值** 的指標，如果不支援遠端設定，則為 TRUE，否則為 **FALSE** 。

</dd> <dt>

*remoteConfigType* \[擴展\]
</dt> <dd>

使用 [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) 列舉中的值，指出支援的遠端設定類型：



| 值                                                                                                 | 意義                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) 會實作為。<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) 會實作為。 您可以使用 DCOM 從遠端呼叫 [**INapComponentConfig：： GetConfig**](inapcomponentconfig-getconfig.md)和 [**INapComponentConfig：： SetConfig**](inapcomponentconfig-setconfig.md) 。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功或其中一個標準 Windows 錯誤碼，則會傳回 S OK。

## <a name="remarks"></a>備註

如果 [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) 和 [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) 都未執行，則無法遠端設定 SHV。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





