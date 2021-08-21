---
title: IDeliveryOptimizationJob2：： GetProperty 方法
description: 傳回 DO 作業的單一屬性。
keywords:
- GetProperty 方法
- GetProperty 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811249"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2：： GetProperty 方法

這個方法會傳回 DO 作業的單一屬性。

## <a name="syntax"></a>語法

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*propId* \[在\]
</dt> <dd>

要取得的必要屬性識別碼。 只支援 VT_BSTR 類型的 **DOJobPropertyId_ExtendedErrorInfo** 。

</dd> <dt>

*propValue* \[擴展\]
</dt> <dd>

結果屬性值，儲存在 VARIANT 型別中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 HRESULT 值。

| 傳回碼                  | 描述          |
|------------------------------|----------------------|
| **S_OK**                     | Success              |
| **DO_E_UNKNOWN_PROPERTY_ID** | 未知的屬性識別碼。 |

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

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
