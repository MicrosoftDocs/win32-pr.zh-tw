---
title: 'IVMVirtualMachine TurnOff 方法 (VPCCOMInterfaces .h) '
description: 關閉虛擬機器。
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- TurnOff 方法 Virtual PC
- TurnOff 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，TurnOff 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025354"
---
# <a name="ivmvirtualmachineturnoff-method"></a>IVMVirtualMachine：： TurnOff 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

關閉虛擬機器。

## <a name="syntax"></a>語法


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*turnOffTask* \[退出，retval\]
</dt> <dd>

[**IVMTask**](ivmtask.md)物件，用來追蹤虛擬機器 turnoff 序列的完成進度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | Description                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                | 作業成功。<br/>                                                     |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                  | 參數為 **Null**。<br/>                                                        |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 呼叫端必須具有執行存取權限，才能關閉此虛擬機器。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                     | 虛擬機器未執行。<br/>                                               |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                          | 未知的設定。<br/>                                                     |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                          | 已發生未預期的錯誤。<br/>                                                 |



 

## <a name="remarks"></a>備註

這個方法會關閉虛擬機器的方式，就像在實體機器上關閉電源一樣。

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

 

