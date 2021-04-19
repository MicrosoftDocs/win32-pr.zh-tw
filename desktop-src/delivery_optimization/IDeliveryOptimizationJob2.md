---
title: IDeliveryOptimizationJob2 介面
description: 深入瞭解： IDeliveryOptimizationJob2 介面
keywords:
- IDeliveryOptimizationJob2 介面
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970928"
---
# <a name="ideliveryoptimizationjob2-interface"></a>IDeliveryOptimizationJob2 介面

IDeliveryOptimizationJob2 可讓您將單一檔案新增至下載作業，並立即取出檔案。 這個介面也支援設定和取得選擇性的工作屬性。

## <a name="members"></a>成員

**IDeliveryOptimizationJob2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDeliveryOptimizationJob2** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IDeliveryOptimizationJob2** 介面具有這些方法。

| 方法                                              | 描述                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | AddFile 方法會將單一檔案新增至現有的作業。         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | AddFile 方法會將單一檔案新增至現有的作業。 |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | 未使用這個方法。                                       |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 10， \[ 僅限1803版桌面應用程式\]                                   |
| 最低支援的伺服器 | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]                               |
| 標頭                   | >deliveryoptimization。h                                                           |
| Idl                      | >deliveryoptimization .idl                                                         |
| 程式庫                  | Dosvc .lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
