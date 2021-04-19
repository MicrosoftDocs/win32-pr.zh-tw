---
description: 設定媒體資料流程來源的範例。
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: IMFMediaStreamSourceSampleRequest：： SetSample 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997600"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a>IMFMediaStreamSourceSampleRequest：： SetSample 方法

設定媒體資料流程來源的範例。

## <a name="syntax"></a>語法


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

媒體資料流程來源的範例。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaStreamSourceSampleRequest**](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




