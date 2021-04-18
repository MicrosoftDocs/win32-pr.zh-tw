---
title: IDeliveryOptimizationJob2：： SetProperty 方法
description: 未使用這個方法。
keywords:
- SetProperty 方法
- SetProperty 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384777"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>IDeliveryOptimizationJob2：： SetProperty 方法

未使用這個方法。

## <a name="syntax"></a>語法

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*propId* \[在\]
</dt> <dd>

未使用的。

</dd> <dt>

*propValue* \[在\]
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **DOJobPropertyId_ExtendedErrorInfo** propId，則傳回的值會 **DO_E_READ_ONLY_PROPERTY**，否則函數會傳回 **DO_E_UNKNOWN_PROPERTY_ID**。

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

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
