---
title: 'IWMDRMIndividualizationStatus GetStatus 方法 (Wmdrmsdk .h) '
description: GetStatus 方法會抓取有關「個人化進度」的詳細資訊。
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- GetStatus 方法 windows Media 格式
- GetStatus 方法 windows Media Format，IWMDRMIndividualizationStatus 介面
- IWMDRMIndividualizationStatus 介面 windows Media Format，GetStatus 方法
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994104"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>IWMDRMIndividualizationStatus：： GetStatus 方法

**GetStatus** 方法會抓取有關「個人化進度」的詳細資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStatus* \[擴展\]
</dt> <dd>

接收 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md) 結構，其中包含有關「個人化嘗試」狀態的詳細資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMIndividualizationStatus 介面**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





