---
title: 'IWMDRMNetReceiver GetRegistrationChallenge 方法 (Wmdrmsdk .h) '
description: GetRegistrationChallenge 方法會產生網路裝置註冊挑戰訊息的 Windows 媒體 DRM。
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- GetRegistrationChallenge 方法 windows Media 格式
- GetRegistrationChallenge 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，GetRegistrationChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701033"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>IWMDRMNetReceiver：： GetRegistrationChallenge 方法

**GetRegistrationChallenge** 方法會產生網路裝置註冊挑戰訊息的 Windows 媒體 DRM。

## <a name="syntax"></a>語法


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppbRegistrationChallenge* \[擴展\]
</dt> <dd>

接收所產生之挑戰位址的指標位址。 完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> <dt>

*pcbRegistrationChallenge* \[擴展\]
</dt> <dd>

接收註冊挑戰大小的變數位址（以位元組為單位）。

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

[**IWMDRMNetReceiver：:P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





