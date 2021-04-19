---
title: 'IWMDRMNetReceiver ProcessRegistrationResponse 方法 (Wmdrmsdk .h) '
description: ProcessRegistrationResponse 方法會在回復註冊挑戰時，處理傳輸器所傳送的註冊回應。
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- ProcessRegistrationResponse 方法 windows Media 格式
- ProcessRegistrationResponse 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，ProcessRegistrationResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977162"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>IWMDRMNetReceiver：:P rocessRegistrationResponse 方法

**ProcessRegistrationResponse** 方法會在回復註冊挑戰時，處理傳輸器所傳送的註冊回應。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbRegistrationResponse* \[在\]
</dt> <dd>

從傳輸器收到的註冊回應。

</dd> <dt>

*cbRegistrationResponse* \[在\]
</dt> <dd>

註冊回應的大小（以位元組為單位）。

</dd> <dt>

*ppunkCancellationCookie* \[擴展\]
</dt> <dd>

指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。 這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會以非同步方式執行;當處理完成時，MEProximityCompleted 事件會傳送至 **IMFMediaEventGenerator** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNetReceiver 介面**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





