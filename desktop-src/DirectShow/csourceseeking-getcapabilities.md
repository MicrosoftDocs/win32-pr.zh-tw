---
description: CSourceSeeking. GetCapabilities 方法-GetCapabilities 方法會抓取資料流程的所有搜尋功能。 這個方法會實 IMediaSeeking：： GetCapabilities 方法。
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: 'CSourceSeeking. GetCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96e3a637673a91ebc98e48777b8f42bdcbf02654a0c264037a66b4121f5b80ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054338"
---
# <a name="csourceseekinggetcapabilities-method"></a>CSourceSeeking. GetCapabilities 方法

方法會抓取 `GetCapabilities` 資料流程的所有搜尋功能。 這個方法會實 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCapabilities* 
</dt> <dd>

變數的指標，此變數會接收搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 旗標之 AM 的位元組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | 描述                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="remarks"></a>備註

搜尋功能是由 [**CSourceSeeking：： m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) 成員變數所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




