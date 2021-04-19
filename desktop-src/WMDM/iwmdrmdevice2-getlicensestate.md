---
title: IWMDRMDevice2 GetLicenseState 方法
description: GetLicenseState 方法會取得授權狀態。
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- GetLicenseState 方法 windows Media 裝置管理員
- GetLicenseState 方法 windows Media 裝置管理員，IWMDRMDevice2 介面
- IWMDRMDevice2 interface windows Media 裝置管理員，GetLicenseState 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991258"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2：： GetLicenseState 方法

**GetLicenseState** 方法會取得授權狀態。

## <a name="syntax"></a>語法


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbStateQueryData* \[在\]
</dt> <dd>

授權狀態的查詢資料指標。

</dd> <dt>

*cbStateQueryData* \[在\]
</dt> <dd>

查詢的資料計數。

</dd> <dt>

*pdwCategory* \[擴展\]
</dt> <dd>

類別的指標。

</dd> <dt>

*pcRemainingCounts* \[擴展\]
</dt> <dd>

剩餘計數的指標。

</dd> <dt>

*pcRemainingHours* \[擴展\]
</dt> <dd>

剩餘時數的指標。

</dd> <dt>

*pdwReserved* \[擴展\]
</dt> <dd>

保留供未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 方法成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice2 介面**](iwmdrmdevice2.md)
</dt> </dl>

 

 





