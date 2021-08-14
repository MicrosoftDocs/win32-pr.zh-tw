---
title: 'IVMVirtualMachine DetachUSBDevice 方法 (VPCCOMInterfaces .h) '
description: 從虛擬機器釋放 USB 裝置。
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice 方法 Virtual PC
- DetachUSBDevice 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DetachUSBDevice 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5b45821f56a9533ed851f6c73342fbd15801223832cf9bad9a380b3f97f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344672"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine：:D etachUSBDevice 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

從虛擬機器釋放 USB 裝置。

## <a name="syntax"></a>語法


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inUSBDevice* \[在\]
</dt> <dd>

[**IVMUSBDevice**](ivmusbdevice.md)指標，代表要從虛擬機器卸離的 USB 裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                          | Description                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                | 作業成功。<br/>       |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                  | 參數為 **Null**。<br/>          |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>     | 虛擬機器未執行。<br/> |
| <dl> <dt>**VM \_E \_ USB 卸 \_ 離 \_ 失敗**</dt> <dt>0xA00400927</dt> </dl> | 卸離作業失敗。<br/>        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>          | 已發生未預期的錯誤。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

