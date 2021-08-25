---
description: 將虛擬機器中執行之應用程式的健全狀況狀態回報給在相同虛擬機器中執行的 Hyper-v 整合元件。
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: IVmApplicationHealthMonitor 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 3cc565c43fd61ebed6183cbfa2f4fdf7ece7d39872f23718fb1a12a3b591d531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694318"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>IVmApplicationHealthMonitor 介面

將虛擬機器中執行之應用程式的健全狀況狀態回報給在相同虛擬機器中執行的 Hyper-v 整合元件。 在虛擬機器中執行之應用程式的狀態會反映在 \[ \] [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md)類別的 OperationalStatus 1 屬性值中。 此介面也會提供一種方法，以重設所有在 Hyper-v 中累積的應用程式狀態。

此介面是由 Windows 8 hyper-v 整合元件所執行。 藉由建立 **397A2e5f-348c-482d-b9a3-57d383b483cd** CLSID 的實例，即可取得這個介面的實例。

## <a name="members"></a>成員

**IVmApplicationHealthMonitor** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVmApplicationHealthMonitor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IVmApplicationHealthMonitor** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | 重設虛擬機器中所有應用程式的健全狀況狀態。<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | 設定在虛擬機器中執行之應用程式的健全狀況狀態。<br/> |



 

## <a name="remarks"></a>備註

若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                                                                                           |
| 版本<br/>                  | Windows 8 的整合元件<br/>                                                                                                                                |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor .idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor 定義為267a0284-848f-447e-a096-5e10a1a76bca<br/> 物件識別碼定義為397a2e5f-348c-482d-b9a3-57d383b483cd<br/> |



 

