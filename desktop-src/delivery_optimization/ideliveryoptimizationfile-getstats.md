---
title: 'IDeliveryOptimizationFile GetStats 方法 (>deliveryoptimization .h) '
description: 傳回特定檔案的下載和上傳統計資料。
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats 方法
- GetStats 方法，IDeliveryOptimizationFile 介面
- IDeliveryOptimizationFile 介面，GetStats 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385089"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>IDeliveryOptimizationFile：： GetStats 方法

傳回特定檔案的下載和上傳統計資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*swarmStats* \[擴展\]
</dt> <dd>

傳回特定檔案的下載和上傳統計資料。 如需詳細資訊，請參閱 [**DOSwarmStats**](doswarmstats.md) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法應該會傳回 **S_OK**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile 定義為 B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





