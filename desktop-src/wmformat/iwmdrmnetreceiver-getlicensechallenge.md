---
title: 'IWMDRMNetReceiver GetLicenseChallenge 方法 (Wmdrmsdk .h) '
description: GetLicenseChallenge 方法會產生網路裝置的 Windows Media DRM 授權挑戰，可在要求受保護的內容時傳送給發送器。
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- GetLicenseChallenge 方法 windows Media 格式
- GetLicenseChallenge 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，GetLicenseChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994199"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>IWMDRMNetReceiver：： GetLicenseChallenge 方法

**GetLicenseChallenge** 方法會產生網路裝置的 WINDOWS Media DRM 授權挑戰，可在要求受保護的內容時傳送給發送器。

## <a name="syntax"></a>語法


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAction* \[在\]
</dt> <dd>

要產生挑戰的動作。

</dd> <dt>

*ppbLicenseChallenge* \[擴展\]
</dt> <dd>

設定為所產生挑戰位址之指標的位址。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> <dt>

*pcbLicenseChallenge* \[擴展\]
</dt> <dd>

接收授權挑戰大小的變數位址（以位元組為單位）。

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

[**IWMDRMNetReceiver 介面**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver：:P rocessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





