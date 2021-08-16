---
title: IBasicDevice RemoteStreamingUrls 方法
description: 傳回遠端串流 Url 的向量。
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- RemoteStreamingUrls 方法媒體串流 API
- RemoteStreamingUrls 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，RemoteStreamingUrls 方法
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972327"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>IBasicDevice：： RemoteStreamingUrls 方法

傳回遠端串流 Url 的向量。

## <a name="syntax"></a>語法


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收遠端串流 Url 之指標的可列舉集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





