---
description: NOTE 宏會將字串傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: '注意 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990811"
---
# <a name="note"></a>注意

`NOTE`宏會將字串傳送至調試輸出位置。 在零售組建中略過。

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*Pformatetc 架構*
</dt> <dd>

Printf 樣式的格式字串。

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*
</dt> <dd>

格式字串的其他引數。 引數的數目必須符合宏名稱。 例如， **NOTE1** 會採用一個引數，而 **NOTE5** 會採用五個引數。

</dd> </dl>

## <a name="remarks"></a>備註

這些宏是 [**DbgLog**](dbglog.md) 宏的變體。 它們會產生層級5記錄 \_ 追蹤訊息。

## <a name="example"></a>範例


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




