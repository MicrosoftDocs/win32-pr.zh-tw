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
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986058"
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

| 傳回碼                  | Description                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Success                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | 未知的屬性識別碼                                                |
| **DO_E_INVALID_STATE**       | 作業目前不在允許屬性設定的狀態 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|---------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端  | Windows 10， \[ 僅限1803版桌面應用程式\]                                   |
| 最低支援的伺服器  | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]                               |
| 標頭                    | >deliveryoptimization。h                                                           |
| Idl                       | >deliveryoptimization .idl                                                         |
| 程式庫                   | Dosvc .lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>另請參閱

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
