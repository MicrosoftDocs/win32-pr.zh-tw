---
title: 'IVMVirtualMachine RemoveNetworkAdapter 方法 (VPCCOMInterfaces .h) '
description: 從虛擬機器移除網路介面。
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- RemoveNetworkAdapter 方法 Virtual PC
- RemoveNetworkAdapter 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveNetworkAdapter 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4f233b0cc8262a1d339d04ffe862e5e10456c8ffed431e4b4bf74eb5268d0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333358"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a>IVMVirtualMachine：： RemoveNetworkAdapter 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

從虛擬機器移除網路介面。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*networkAdapter* \[在\]
</dt> <dd>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)物件，代表要移除的網路介面卡。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                            | Description                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                       |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                    | 參數為 **Null**。<br/>                          |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                       |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl> | 虛擬機器處於執行中或已儲存狀態。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                   |



 

## <a name="remarks"></a>備註

您只能從已停止的虛擬機器中移除現有的網路介面。

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

 

