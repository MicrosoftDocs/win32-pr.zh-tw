---
title: 'IWMDRMNetTransmitter GetLeafLicenseResponse 方法 (Wmdrmsdk .h) '
description: GetLeafLicenseResponse 方法會產生分葉授權回應訊息。
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- GetLeafLicenseResponse 方法 windows Media 格式
- GetLeafLicenseResponse 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，GetLeafLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982543"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>IWMDRMNetTransmitter：： GetLeafLicenseResponse 方法

**GetLeafLicenseResponse** 方法會產生分葉授權回應訊息。

## <a name="syntax"></a>語法


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

要用於新分葉授權的 Base64 編碼金鑰識別碼。 金鑰識別碼應為隨機產生的 GUID 值。

</dd> <dt>

*pPolicy* \[在\]
</dt> <dd>

[**WMDRMNET \_ 原則**](wmdrmnet-policy.md)結構的指標，該結構定義要用於分葉授權的原則。

</dd> <dt>

*ppIWMDRMEncrypt* \[擴展\]
</dt> <dd>

接收 [**IWMDRMEncrypt**](iwmdrmencrypt.md) 介面指標的變數位址，該介面可用來加密新分葉授權的資料。

</dd> <dt>

*ppbLicenseResponse* \[擴展\]
</dt> <dd>

接收產生的授權回應位址之變數的位址。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> <dt>

*pcbLicenseResponse* \[擴展\]
</dt> <dd>

接收授權回應大小的變數位址（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNetTransmitter 介面**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





