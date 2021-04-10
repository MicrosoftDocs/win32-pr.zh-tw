---
title: IDeliveryOptimizationFile2 介面
description: IDeliveryOptimizationFile2 支援設定和取得選用的檔案屬性。
keywords:
- IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024865"
---
# <a name="ideliveryoptimizationfile2-interface"></a>IDeliveryOptimizationFile2 介面

**IDeliveryOptimizationFile2** 支援設定和取得選用的檔案屬性。 

## <a name="members"></a>成員

**IDeliveryOptimizationFile2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDeliveryOptimizationFile2** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IDeliveryOptimizationFile2** 介面具有這些方法。

| 方法                                                 | 描述                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | 這個方法會傳回 DO 檔案的單一屬性。 |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | 這個方法會設定 DO 檔案的單一屬性。    |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端      | Windows 10， \[ 僅限1803版桌面應用程式\]                                    |
| 最低支援的伺服器      | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]                                |
| 標頭                        | >deliveryoptimization。h                                                            |
| Idl                           | >deliveryoptimization .idl                                                          |
| 程式庫                       | Dosvc .lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 定義為3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
