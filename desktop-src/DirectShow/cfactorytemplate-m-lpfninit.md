---
description: 從 DLL 進入點呼叫之函式的指標。 可以是 NULL。
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'CFactoryTemplate：： m_lpfnInit 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9f4a12c03e7e001845437f57f9799c7b0861f4f8f9b6cfac56aaa2bb80e51a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566918"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>CFactoryTemplate：： m \_ lpfnInit 成員

從 DLL 進入點呼叫之函式的指標。 可以是 **Null**。

## <a name="syntax"></a>語法


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>備註

函數指標型別為 [**LPFNInitRoutine**](lpfninitroutine.md)。 如果您在 DLL 中提供此函式，DLL 進入點函數會使用下列參數來呼叫它：

-   *bLoading*：載入 dll 時 **為 TRUE** ，卸載 dll 時為 **FALSE** 。
-   *rclsid*：物件之 CLISD 的指標，在 [**CFactoryTemplate：： m \_ ClsID**](cfactorytemplate-m-clsid.md) 成員變數中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 




