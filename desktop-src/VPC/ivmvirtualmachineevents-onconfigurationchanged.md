---
title: 'IVMVirtualMachineEvents OnConfigurationChanged 方法 (VPCCOMInterfaces .h) '
description: 接收此虛擬機器設定中的值已變更的通知。
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- OnConfigurationChanged 方法 Virtual PC
- OnConfigurationChanged 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnConfigurationChanged 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056636"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>IVMVirtualMachineEvents：： OnConfigurationChanged 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

接收此虛擬機器設定中的值已變更的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configKey* \[在\]
</dt> <dd>

設定中已變更的值。

</dd> <dt>

*configData* \[在\]
</dt> <dd>

設定的新值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此虛擬機器的設定變更時，會呼叫此方法。 用戶端程式必須執行這個介面方法，以接收來自 IVMVirtualMachine 的 vmVirtualMachineEvent \_ ConfigurationChanged 事件的[](ivmvirtualmachine.md)通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

