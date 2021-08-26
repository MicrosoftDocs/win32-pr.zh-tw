---
description: CBasePin 中斷連接方法-中斷連接方法會中斷目前的 pin 連線。 這個方法會實 IPin：:D isconnect 方法。
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: 'CBasePin 連接方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0048624b79daa6948851fd9a56142b97c7e185caa9bbcbdeb6c2c1b19f591eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916628"
---
# <a name="cbasepindisconnect-method"></a>CBasePin 中斷方法

`Disconnect`方法會中斷目前的 pin 連接。 這個方法會實 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                         | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Pin 未連接。<br/>                                              |
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 成功。<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl> | 篩選準則為使用中，且 pin 不支援動態重新連接。<br/> |



 

## <a name="remarks"></a>備註

基類會將大部分的工作委派給 [**CBasePin：:D isconnectinternal**](cbasepin-disconnectinternal.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




