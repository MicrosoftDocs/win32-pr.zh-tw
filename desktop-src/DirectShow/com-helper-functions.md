---
description: 這些函數可支援在 DirectShow 中執行 IUnknown 介面。
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: 'COM Helper 函數 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084338"
---
# <a name="com-helper-functions"></a>COM Helper 函數

這些函數可支援在 DirectShow 中執行 **IUnknown** 介面。



| 函式                                               | 描述                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**宣告 \_ IUNKNOWN**](declare-iunknown.md)          | 針對新介面宣告基底介面的三種方法。 |
| [**GetInterface**](getinterface.md)                   | 抓取所要求用戶端的介面指標。               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | **IUnknown** 介面的 Nondelegating 版本。                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | 載入 Automation DLL (OleAut32.dll) 。                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[公用程式函數](utility-functions.md)
</dt> </dl>

 

 




