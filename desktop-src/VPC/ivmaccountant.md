---
title: 'IVMAccountant 介面 (VPCCOMInterfaces .h) '
description: 提供虛擬機器的帳戶計量相關資訊的存取權。
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- IVMAccountant 介面 Virtual PC
- IVMAccountant 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686415"
---
# <a name="ivmaccountant-interface"></a>IVMAccountant 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

提供虛擬機器的帳戶計量相關資訊的存取權。 若要取得虛擬機器的 **IVMAccountant** ，請使用 [**IVMVirtualMachine：：會計師**](ivmvirtualmachine-accountant.md) 屬性。

## <a name="members"></a>成員

**IVMAccountant** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMAccountant** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMAccountant** 介面具有這些屬性。



| 屬性                                                                        | 存取類型          | Description                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPUUtilization**](ivmaccountant-cpuutilization.md)<br/>               | 唯讀<br/> | 此虛擬機器目前的 CPU 使用率百分比。<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | 唯讀<br/> | 此虛擬機器的最近 CPU 使用率 (為百分比值陣列) 。<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | 唯讀<br/> | 此虛擬機器的所有儲存控制器讀取的位元組總數。<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | 唯讀<br/> | 此虛擬機器的所有儲存控制器所寫入的位元組總數。<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | 唯讀<br/> | 此虛擬機器的所有虛擬網路介面卡所接收的位元組總數。<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | 唯讀<br/> | 此虛擬機器的所有虛擬網路介面卡所傳送的位元組總數。<br/>     |
| [**99.99**](ivmaccountant-uptime.md)<br/>                               | 唯讀<br/> | 虛擬機器已執行的秒數。<br/>                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



 

