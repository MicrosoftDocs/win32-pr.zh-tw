---
title: IBasicDevice PresentationUrl 方法
description: 抓取裝置的簡報 URL。
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- PresentationUrl 方法媒體串流 API
- PresentationUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，PresentationUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373000"
---
# <a name="ibasicdevicepresentationurl-method"></a>IBasicDevice：:P resentationUrl 方法

抓取裝置的簡報 URL。

## <a name="syntax"></a>語法


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收裝置展示 URL 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





