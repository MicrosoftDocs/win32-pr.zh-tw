---
title: 'IVMVirtualMachine HasSSE 屬性 (VPCCOMInterfaces .h) '
description: '判斷處理器是否支援 SSE 指令集。 |IVMVirtualMachine HasSSE 屬性 (VPCCOMInterfaces .h) '
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- HasSSE 屬性 Virtual PC
- HasSSE 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，HasSSE 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853907"
---
# <a name="ivmvirtualmachinehassse-property"></a>IVMVirtualMachine：： HasSSE 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷處理器是否支援 SSE 指令集。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a>屬性值

如果處理器支援 SSE 指令集，**則為 TRUE** ，否則為 **FALSE** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>     |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



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

 

