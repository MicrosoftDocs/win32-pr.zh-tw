---
title: 'IWMDRMNetReceiver ProcessLicenseResponse 方法 (Wmdrmsdk .h) '
description: ProcessLicenseResponse 方法會處理傳輸器在回復至授權挑戰時傳送的授權回應。
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- ProcessLicenseResponse 方法 windows Media 格式
- ProcessLicenseResponse 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，ProcessLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700822"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>IWMDRMNetReceiver：:P rocessLicenseResponse 方法

**ProcessLicenseResponse** 方法會處理傳輸器在回復至授權挑戰時傳送的授權回應。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbLicenseResponse* \[在\]
</dt> <dd>

從傳輸器收到的授權回應。

</dd> <dt>

*cbLicenseResponse* \[在\]
</dt> <dd>

回應的大小（以位元組為單位）。

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[擴展\]
</dt> <dd>

變數的位址，此變數會接收授權回應訊息中所含授權之內部授權表示的位址。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。 如果不需要授權標記法，此參數可以設定為 **Null** 。

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[擴展\]
</dt> <dd>

接收授權表示大小之變數的位址。 如果 *ppbWMDRMNetLicenseRepresentation* 為 **null**，則必須設定為 **null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | 描述                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

使用這個方法所處理的授權回應必須對應至用戶端電腦上所產生的最後一個授權挑戰。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNetReceiver 介面**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





