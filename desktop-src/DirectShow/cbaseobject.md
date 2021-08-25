---
description: CBaseObject 類別是用來執行 DirectShow 物件的抽象類別。 若要執行元件物件模型 (COM) 物件，請使用衍生自 CBaseObject 的 CUnknown 類別。
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: 'CBaseObject 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7809ec53746730f02f9b095ede3ae00b53f1fe55c21116c22d854c3d4b193e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910618"
---
# <a name="cbaseobject-class"></a>CBaseObject 類別

**CBaseObject** 類別是用來執行 DirectShow 物件的抽象類別。 若要執行元件物件模型 (COM) 物件，請使用衍生自 **CBaseObject** 的 [**CUnknown**](cunknown.md)類別。



| 類別方法                                      | 描述                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | 函式方法。                    |
| [**~ CBaseObject**](cbaseobject--cbaseobject.md)   | 函式方法。                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | 捕獲使用中物件的計數。 |



 

## <a name="remarks"></a>備註

大部分的 DirectShow 基類衍生自 **CBaseObject**。 這個類別會藉由保留在執行時間中使用中的所有 DirectShow 物件計數，來提供偵錯工具的協助。 物件計數會儲存在類別靜態成員變數中：


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



在「偵錯工具」組建中，如果物件計數大於零，則會判斷提示 DLL 是否已卸載。 這可讓您更輕鬆地追蹤參考計數問題所造成的流失問題。

**CBaseObject** 的函式會接受一個引數，也就是物件的偵錯工具名稱。 這個名稱會儲存在 DLL 的全域資料表中。 [**DbgDumpObjectRegister**](dbgdumpobjectregister.md)函式會格式化 DLL 中的作用中物件清單，並將其傳送至 debug 輸出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> </dl>

 

 




