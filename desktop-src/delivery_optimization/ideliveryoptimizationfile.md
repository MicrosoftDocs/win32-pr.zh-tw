---
title: IDeliveryOptimizationFile 介面
description: 執行 IDeliveryOptimizationFile 介面，以識別特定檔案的狀態。
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- IDeliveryOptimizationFile 介面
- IDeliveryOptimizationFile 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635738"
---
# <a name="ideliveryoptimizationfile-interface"></a>IDeliveryOptimizationFile 介面

執行 **IDeliveryOptimizationFile** 介面，以識別特定檔案的狀態。

## <a name="members"></a>成員

**IDeliveryOptimizationFile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDeliveryOptimizationFile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDeliveryOptimizationFile** 介面具有這些方法。



| 方法                                                 | 描述                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | 傳回特定檔案的下載和上傳統計資料。<br/> |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端      | Windows 10， \[ 僅限1709版桌面應用程式\]                                   |
| 最低支援的伺服器      | WindowsServer， \[ 僅限1709版桌面應用程式\]                               |
| 標頭                        | >Deliveryoptimization。h                                                           |
| IDL                           | >deliveryoptimization .idl                                                         |
| 程式庫                       | Dosvc .lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile 定義為 B76B9699-E99E-4101-803F-A20E325D93E2 |
