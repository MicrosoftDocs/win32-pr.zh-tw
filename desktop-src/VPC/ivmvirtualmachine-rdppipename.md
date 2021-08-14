---
title: 'IVMVirtualMachine RdpPipeName 屬性 (VPCCOMInterfaces .h) '
description: 抓取用於影片和輸入的 RDP 連接具名管道名稱。
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- RdpPipeName 屬性 Virtual PC
- RdpPipeName 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RdpPipeName 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0616cd36e35690649cac145b9462b96af19499e3a10f7fdee3ec2820891544d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394448"
---
# <a name="ivmvirtualmachinerdppipename-property"></a>IVMVirtualMachine：： RdpPipeName 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取用於影片和輸入的 RDP 連接具名管道名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a>屬性值

用於影片和輸入的 RDP 連接具名管道的名稱。

## <a name="error-codes"></a>錯誤碼

如果方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。



| 名稱/值                                                                                                                                                         | 意義                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>          |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>              | RdpPipeName 參數為 **Null**。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl> | 虛擬機器未執行。<br/>    |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>      | 發生未知的錯誤。<br/>             |



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

 

