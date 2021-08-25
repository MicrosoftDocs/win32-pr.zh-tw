---
description: DisplayType 函式會將媒體類型的相關資訊傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: 'DisplayType 函數 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a48bc5f4afbfabc9bdc37ff2cfe8c5890629f3fcaacf135979b82523981ed66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906498"
---
# <a name="displaytype-function"></a>DisplayType 函數

函式會 `DisplayType` 將媒體類型的相關資訊傳送至調試輸出位置。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*label* 
</dt> <dd>

包含要以媒體類型資訊顯示之訊息的字串。

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer 至包含媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數會產生數個記錄 \_ 追蹤訊息。 在記錄層級2或更高版本中，此函式會顯示主要類型、子類型和格式類型，以及來自格式區塊的資料。 在記錄層級5或更高時，此函式會顯示其他資訊，例如影片類型的來源和目標矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




