---
title: 'INapComponentConfig InvokeUI 方法 (NapCommon .h) '
description: 針對 (SHV) 元件的系統健全狀況驗證程式啟動自訂使用者介面。
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- InvokeUI 方法 NAP
- InvokeUI 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，InvokeUI 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934172"
---
# <a name="inapcomponentconfiginvokeui-method"></a>INapComponentConfig：： InvokeUI 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**InvokeUI** 方法會針對 (SHV) 元件的系統健全狀況驗證程式啟動自訂使用者介面。

## <a name="syntax"></a>語法


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

父系或擁有者視窗的控制碼。 必須提供有效的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>       | SHV 不支援自訂的 UI。<br/>               |



 

## <a name="remarks"></a>備註

此方法呼叫應該會封鎖，直到 SHV 使用者介面結束為止。

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

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





