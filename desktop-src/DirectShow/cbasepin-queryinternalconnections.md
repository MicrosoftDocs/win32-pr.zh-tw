---
description: QueryInternalConnections 方法會將在內部連接的釘選到篩選) 內 (的釘選。 這個方法會實 IPin：： QueryInternalConnections 方法。
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: 'CBasePin. QueryInternalConnections 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983045"
---
# <a name="cbasepinqueryinternalconnections-method"></a>CBasePin. QueryInternalConnections 方法

`QueryInternalConnections`方法會將在內部連接的釘選到篩選) 內 (的釘選。 這個方法會實 [**IPin：： QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*apPin* 
</dt> <dd>

[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)指標陣列的位址。

</dd> <dt>

*nPin* 
</dt> <dd>

在 [輸入] 上，指定陣列的大小。 當方法傳回時，值會設定為數組中傳回的指標數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 陣列大小不足。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                 |
| <dl> <dt>**E \_ 失敗**</dt> </dl>    | 失敗。<br/>                 |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 未實作。<br/>         |



 

## <a name="remarks"></a>備註

在某些篩選器上，輸入圖釘會對應到特定的輸出圖釘。 針對每個圖釘，此方法會在陣列中填入對應的釘選指標。 如果每個輸入 pin 都提供每個輸出 pin 的資料，則傳回 E \_ >notimpl。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




