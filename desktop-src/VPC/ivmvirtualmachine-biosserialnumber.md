---
title: 'IVMVirtualMachine BIOSSerialNumber 屬性 (VPCCOMInterfaces .h) '
description: BIOS 序號。
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- BIOSSerialNumber 屬性 Virtual PC
- BIOSSerialNumber 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，BIOSSerialNumber 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8bd3f240d863a6f43dabbdb0a26429c4a77219
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025398"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a>IVMVirtualMachine：： BIOSSerialNumber 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捕獲並設定 BIOS 序號。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a>屬性值

指定 BIOS 序號。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                               | 意義                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                                               |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                    | 參數為 **Null**。<br/>                                                  |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | 參數大於32個字元、空字串或無效。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                                               |
| <dl> <dt>VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的</dt> <dt>0xA004020B</dt> </dl> | 虛擬機器處於執行中或已儲存狀態。<br/>                         |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                                           |



## <a name="remarks"></a>備註

在虛擬機器第一次啟動之後，此屬性才會包含有效的資訊。 如果在初始啟動之前讀取了空字串，則會傳回空字串。

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

 

