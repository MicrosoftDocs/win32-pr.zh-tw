---
title: 'IVMVirtualMachine AddNetworkAdapter 方法 (VPCCOMInterfaces .h) '
description: 將網路介面新增至虛擬機器。
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter 方法 Virtual PC
- AddNetworkAdapter 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddNetworkAdapter 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966940"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>IVMVirtualMachine：： AddNetworkAdapter 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將網路介面新增至虛擬機器。

## <a name="syntax"></a>語法


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*networkAdapter* \[退出，retval\]
</dt> <dd>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                            | Description                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                    | *NetworkAdapter* 參數為 **Null**。<br/>          |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                        |
| <dl> <dt>**VM \_E \_ PREF 不 \_ 合法的 \_ 值**</dt> <dt>0xA0040301</dt> </dl>   | 您可以新增四個以上的 (4) 網路介面卡。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl> | 虛擬機器處於執行中或已儲存狀態。<br/>  |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                    |



 

## <a name="remarks"></a>備註

您只能將新的網路介面新增至已停止的虛擬機器。 新建立的網路介面卡未連接至虛擬網路。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

