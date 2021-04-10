---
title: 'IVMVirtualPCEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualPC 介面的外寄事件介面。
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- IVMVirtualPCEvents 介面 Virtual PC
- IVMVirtualPCEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025337"
---
# <a name="ivmvirtualpcevents-interface"></a>IVMVirtualPCEvents 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 [**IVMVirtualPC**](ivmvirtualpc.md) 介面的外寄事件介面。 用戶端會執行這些方法來接收從 [**IVMVirtualPC**](ivmvirtualpc.md)傳送的事件。

## <a name="members"></a>成員

**IVMVirtualPCEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualPCEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IVMVirtualPCEvents** 介面具有這些方法。



| 方法                                                        | 描述                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnEventLogged**](ivmvirtualpcevents-oneventlogged.md)     | 接收 Windows Virtual PC 記錄事件的通知。<br/>      |
| [**OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md) | 收到虛擬機器的狀態已變更的通知。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



 

