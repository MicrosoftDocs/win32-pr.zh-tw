---
title: IWMDRMDevice GetSecureClockChallenge 方法
description: GetSecureClockChallenge 方法會捕獲安全的時鐘挑戰結果。
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- GetSecureClockChallenge 方法 windows Media 裝置管理員
- GetSecureClockChallenge 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSecureClockChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957248"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>IWMDRMDevice：： GetSecureClockChallenge 方法

**GetSecureClockChallenge** 方法會捕獲安全的時鐘挑戰結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppbChallenge* \[擴展\]
</dt> <dd>

已取出挑戰結果。

</dd> <dt>

*pcbChallenge* \[擴展\]
</dt> <dd>

挑戰結果的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





