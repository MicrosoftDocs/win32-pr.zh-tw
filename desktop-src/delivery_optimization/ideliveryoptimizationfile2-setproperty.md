---
title: IDeliveryOptimizationFile2：： SetProperty 方法
description: 這個方法會傳回 DO 檔案的單一屬性。 |IDeliveryOptimizationFile2：： SetProperty 方法
keywords:
- SetProperty 方法
- SetProperty 方法，IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635718"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2：： SetProperty 方法

這個方法會傳回 DO 檔案的單一屬性。

## <a name="syntax"></a>語法

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*propId* \[在\]
</dt> <dd>

要設定 DOFilePropertyId 類型的必要屬性識別碼。

</dd> <dt>

*propValue* \[在\]
</dt> <dd>

要設定的屬性值，屬於 VARIANT 類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 HRESULT 值。

| 傳回碼                  | 描述                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Success                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | 未知的屬性識別碼                                                |
| **DO_E_INVALID_STATE**       | 作業目前不在允許屬性設定的狀態 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|---------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端  | Windows 10， \[ 僅限1803版桌面應用程式\]                                   |
| 最低支援的伺服器  | WindowsServer， \[ 僅限1709版桌面應用程式\]                               |
| 標頭                    | >Deliveryoptimization。h                                                           |
| IDL                       | >deliveryoptimization .idl                                                         |
| 程式庫                   | Dosvc .lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>另請參閱

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
