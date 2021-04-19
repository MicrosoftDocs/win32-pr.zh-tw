---
title: 'IVMVirtualPC DeleteVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 刪除虛擬機器設定。
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine 方法 Virtual PC
- DeleteVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，DeleteVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968189"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC：:D eleteVirtualMachine 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

刪除虛擬機器設定。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*virtualMachine* \[在\]
</dt> <dd>

[**IVMVirtualMachine**](ivmvirtualmachine.md)物件的指標，代表要刪除的虛擬機器設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**S \_FALSE**</dt> <dt>1</dt> </dl>                                           | 找不到指定的設定。<br/>                                      |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *VirtualMachine* 參數為 **Null**。<br/>                                         |
| <dl> <dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt> </dl>                        | 虛擬機器未執行。<br/>                                                      |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |



 

## <a name="remarks"></a>備註

只有已停止的虛擬機器可以刪除。 請注意，除了設定檔案之外，也會刪除此設定的任何現有儲存狀態或復原磁片磁碟機資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

