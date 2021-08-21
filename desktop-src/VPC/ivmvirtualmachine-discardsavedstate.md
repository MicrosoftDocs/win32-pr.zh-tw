---
title: 'IVMVirtualMachine DiscardSavedState 方法 (VPCCOMInterfaces .h) '
description: 捨棄已儲存之虛擬機器的任何儲存狀態資訊。
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState 方法 Virtual PC
- DiscardSavedState 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DiscardSavedState 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff30406328ae13004505440ae2fb8b18b2e1fdf8ac19dcbfbe77b063e54df688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471978"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine：:D iscardSavedState 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捨棄已儲存之虛擬機器的任何儲存狀態資訊。

## <a name="syntax"></a>語法


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                           | Description                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                 | 作業成功。<br/>                               |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>           | 未知的設定。<br/>                               |
| <dl> <dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt> </dl>           | 虛擬機器未執行。<br/>                             |
| <dl> <dt>**VM \_E \_ VM \_ 沒有 \_ 儲存的 \_ 狀態**</dt> <dt>0xA00400501</dt> </dl> | 虛擬機器未執行，但沒有儲存的狀態。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>           | 已發生未預期的錯誤。<br/>                           |



 

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

 

