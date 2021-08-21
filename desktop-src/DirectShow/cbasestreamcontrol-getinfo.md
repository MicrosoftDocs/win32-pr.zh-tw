---
description: GetInfo 方法會抓取目前資料流程控制設定的相關資訊，包括開始和停止時間。 這個方法會實 IAMStreamControl：： GetInfo 方法。
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: 'CBaseStreamControl. GetInfo 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96bc59b6dc55d73aa16b08f53f831428ae2d2fb7b181d3bb255b61a323b236a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157215"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>CBaseStreamControl. GetInfo 方法

方法會抓取 `GetInfo` 目前資料流程控制設定的相關資訊，包括開始和停止時間。 這個方法會實 [**IAMStreamControl：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* 
</dt> <dd>

呼叫端所配置的 [**AM \_ 資料流程 \_ 資訊**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) 結構的指標，該結構會接收目前的資料流程控制設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseStreamControl 類別**](cbasestreamcontrol.md)
</dt> </dl>

 

 




