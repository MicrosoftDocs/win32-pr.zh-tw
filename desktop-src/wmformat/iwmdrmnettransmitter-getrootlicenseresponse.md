---
title: 'IWMDRMNetTransmitter GetRootLicenseResponse 方法 (Wmdrmsdk .h) '
description: GetRootLicenseResponse 方法會產生根授權回應訊息。
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- GetRootLicenseResponse 方法 windows Media 格式
- GetRootLicenseResponse 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，GetRootLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89389163a9eae66a0dcda14dd6b9699d3db9650140cceac6498b2ab77a4e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707928"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>IWMDRMNetTransmitter：： GetRootLicenseResponse 方法

**GetRootLicenseResponse** 方法會產生根授權回應訊息。

## <a name="syntax"></a>語法


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

以 Base64 編碼的金鑰識別碼，用於新的根授權。 金鑰識別碼應為隨機產生的 GUID 值。

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



| 傳回碼                                                                                                | 描述                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

產生的根授權會使用來自授權挑戰資料的資訊來建立，而該資料會藉由呼叫 [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)針對介面進行處理。

根授權是在產生分葉授權時使用，這是藉由呼叫 [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) 方法來完成。 **IWMDRMNetTransmitter** 介面會維護該使用的根授權複本。

藉由呼叫這個方法所建立的根授權沒有任何原則，且已設定為無法在接收的裝置上保存。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNetTransmitter 介面**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





