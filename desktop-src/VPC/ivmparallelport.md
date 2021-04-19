---
title: 'IVMParallelPort 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的平行埠。
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- IVMParallelPort 介面 Virtual PC
- IVMParallelPort 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965945"
---
# <a name="ivmparallelport-interface"></a>IVMParallelPort 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內的平行埠。 此介面可讓您在虛擬機器內設定平行埠。 您可以從 [**IVMVirtualMachine：:P arallelports**](ivmvirtualmachine-parallelports.md)屬性傳回的 [**IVMParallelPortCollection**](ivmparallelportcollection.md)物件中取出 **IVMParallelPort** 物件。

## <a name="members"></a>成員

**IVMParallelPort** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMParallelPort** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMParallelPort** 介面具有這些方法。



| 方法                              | 描述                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_ID**](ivmparallelport--id.md) | 抓取平行埠的內部識別碼。<br/> |



 

### <a name="properties"></a>屬性

**IVMParallelPort** 介面具有這些屬性。



| 屬性                                        | 存取類型           | Description                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Name**](ivmparallelport-name.md)<br/> | 讀取/寫入<br/> | 平行埠的名稱。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort 定義為097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



 

