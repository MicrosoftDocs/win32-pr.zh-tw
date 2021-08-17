---
title: 'IVMVirtualMachine Pause 方法 (VPCCOMInterfaces. h) '
description: 暫停虛擬機器。
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- 暫停方法虛擬電腦
- 暫停方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine interface Virtual PC，Pause 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbab3da710a66c1e737e02693cb2002452ec11154b1be3da0e3568fea38e59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471478"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine：:P ause 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

暫停虛擬機器 (VM) 。

## <a name="syntax"></a>語法


```C++
HRESULT Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | 描述                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                | 作業成功。<br/>                                     |
| <dl> <dt>**E \_FAIL**</dt> <dt>0x80004005</dt> </dl>                                     | VM 已暫停。<br/>                                         |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 呼叫端必須具有執行存取權限，才能暫停此 VM。<br/> |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                           | 作業未及時完成。<br/>                |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                     | 虛擬機器未執行。<br/>                               |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                          | 未知的設定。<br/>                                     |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                          | 已發生未預期的錯誤。<br/>                                 |



 

## <a name="remarks"></a>備註

**暫停** 不會儲存 VM 的目前狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

