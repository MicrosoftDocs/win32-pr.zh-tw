---
title: IMediaRenderer IsImageSupported 方法
description: 抓取值，指出 DMR 是否能夠顯示影像。
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- IsImageSupported 方法媒體串流 API
- IsImageSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsImageSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967461"
---
# <a name="imediarendererisimagesupported-method"></a>IMediaRenderer：： IsImageSupported 方法

抓取值，指出 DMR 是否能夠顯示影像。

## <a name="syntax"></a>語法


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

布林值，如果 DMR 能夠顯示影像，則為 **True** ，否則為 **False** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





