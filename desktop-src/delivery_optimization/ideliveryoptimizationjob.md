---
title: 'IDeliveryOptimizationJob 介面 (>deliveryoptimization .h) '
description: 使用 IDeliveryOptimizationJob 介面下載檔案範圍。
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- IDeliveryOptimizationJob 介面
- IDeliveryOptimizationJob 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71f978be993e21ad487af5469327b5f66804166a7e5247dffb841f7815b2279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895678"
---
# <a name="ideliveryoptimizationjob-interface"></a>IDeliveryOptimizationJob 介面

使用 **IDeliveryOptimizationJob** 介面下載檔案範圍。

## <a name="members"></a>成員

**IDeliveryOptimizationJob** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDeliveryOptimizationJob** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IDeliveryOptimizationJob** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | 將檔案新增至下載作業，並指定您想要下載的檔案範圍。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

