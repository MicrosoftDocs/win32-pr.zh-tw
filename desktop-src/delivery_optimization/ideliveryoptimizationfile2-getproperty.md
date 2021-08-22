---
title: IDeliveryOptimizationFile2：： GetProperty 方法
description: 這個方法會傳回 DO 檔案的單一屬性。 |IDeliveryOptimizationFile2：： GetProperty 方法
keywords:
- GetProperty 方法
- GetProperty 方法，IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542088"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2：： GetProperty 方法

這個方法會傳回 DO 檔案的單一屬性。

## <a name="syntax"></a>語法

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*propId* \[在\]
</dt> <dd>

要取得類型 DOFilePropertyId 的必要屬性識別碼。

</dd> <dt>

*propValue* \[擴展\]
</dt> <dd>

儲存在變數中的屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 HRESULT 值。

| 傳回碼                  | Description                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Success                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | 未知的屬性識別碼。                                |
| **DO_E_WRITE_ONLY_PROPERTY** | 屬性為僅限寫入，無法讀取。      |
| **E_NOT_SET**                | 未透過 SetProperty 方法設定任何屬性。 |
| **E_OUTOFMEMORY**            |  記憶體配置失敗                          |

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
