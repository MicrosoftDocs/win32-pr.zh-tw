---
title: 'INapComponentConfig IsUISupported 方法 (NapCommon .h) '
description: 指定元件是否支援自訂的使用者介面。
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- IsUISupported 方法 NAP
- IsUISupported 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，IsUISupported 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965299"
---
# <a name="inapcomponentconfigisuisupported-method"></a>INapComponentConfig：： IsUISupported 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**IsUISupported** 方法會指定元件是否支援自訂的使用者介面。

## <a name="syntax"></a>語法


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*isSupported* \[擴展\]
</dt> <dd>

如果元件支援自訂的使用者介面，則為布林 **值** 的指標，如果是，則為 FALSE，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

應該使用 [**INapComponentConfig：： InvokeUI**](inapcomponentconfig-invokeui.md)來啟動元件的自訂使用者介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





