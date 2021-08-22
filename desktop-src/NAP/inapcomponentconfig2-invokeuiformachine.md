---
title: 'INapComponentConfig2 InvokeUIForMachine 方法 (NapCommon .h) '
description: 由系統健康狀態驗證 (Shv) 視需要在指定的電腦上直接管理遠端設定。 這個方法會啟動設定管理 UI。
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- InvokeUIForMachine 方法 NAP
- InvokeUIForMachine 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，InvokeUIForMachine 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940186"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>INapComponentConfig2：： InvokeUIForMachine 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**InvokeUIForMachine** 方法是由系統健康狀態驗證 (shv) 視需要在指定的電腦上直接管理遠端設定。 這個方法會啟動設定管理 UI。

## <a name="syntax"></a>語法


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

父系或擁有者視窗的控制碼。 必須提供有效的視窗控制碼。

</dd> <dt>

*machineName* \[在\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)的指標，其中包含 NAP 用戶端的電腦名稱稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，或其中一個標準 Windows 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





