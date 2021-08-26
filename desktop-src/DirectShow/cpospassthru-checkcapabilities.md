---
description: CheckCapabilities 方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 IMediaSeeking：： CheckCapabilities 方法。
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: 'CPosPassThru. CheckCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108418"
---
# <a name="cpospassthrucheckcapabilities-method"></a>CPosPassThru. CheckCapabilities 方法

`CheckCapabilities`方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCapabilities* 
</dt> <dd>

一或多個搜尋中搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 屬性的位元組合指標。 當方法傳回時，值會指出哪些屬性可供使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




