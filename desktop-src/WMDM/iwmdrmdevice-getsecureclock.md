---
title: IWMDRMDevice GetSecureClock 方法
description: GetSecureClock 方法會抓取安全時鐘，因此可以強制執行以時間為基礎的授權。
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- GetSecureClock 方法 windows Media 裝置管理員
- GetSecureClock 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSecureClock 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9494a594a396550028f083cc2b646f2093f6369ab27ae5494bf70c13628d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619778"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>IWMDRMDevice：： GetSecureClock 方法

**GetSecureClock** 方法會抓取安全時鐘，因此可以強制執行以時間為基礎的授權。

## <a name="syntax"></a>語法


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppbSecureClock* \[擴展\]
</dt> <dd>

已取出安全時鐘。

</dd> <dt>

*pcbSecureClock* \[擴展\]
</dt> <dd>

安全時鐘的大小（以位元組為單位）。

</dd> <dt>

*pdwFlags* \[擴展\]
</dt> <dd>

裝置狀態旗標。 此值必須是下列其中一個旗標。



| 旗標                     | 描述                            |
|--------------------------|----------------------------------------|
| WMDRM \_ 裝置 \_ ISWMDRM   | 裝置支援 Windows 媒體 DRM。 |
| WMDRM \_ 裝置 \_ NEEDCLOCK | 裝置需要時鐘。                |
| 已 \_ 撤銷 WMDRM 裝置 \_   | 裝置已遭撤銷。           |



 

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

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





