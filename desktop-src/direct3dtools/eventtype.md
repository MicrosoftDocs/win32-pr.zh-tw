---
description: 用來表示事件種類的列舉。
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 事件種類列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c3d1f940c0c43f77c499e92c9443f7611c27faea22ab97d130c928b649490ae4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671478"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>事件種類列舉

用來表示事件種類的列舉。

## <a name="syntax"></a>Syntax

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a>常數

<span id="ET_NONE"></span><span id="et_none"></span>**ET \_ 無**  
對應至無事件的值。

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET \_ SESSIONSTART**  
對應至會話開始事件的值。

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET \_ SESSIONEND**  
對應至會話結束事件的值。

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET \_ PROCESSSTART**  
對應至進程開始事件的值。

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET \_ PROCESSEND**  
對應至處理常式結束事件的值。

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET \_ FRAMEBEGIN**  
對應至框架開始事件的值。

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET \_ FRAMEEND**  
對應至框架結束事件的值。 未使用。

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ USEREVENTBEGIN**  
對應至使用者事件開始事件的值。

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ USEREVENTEND**  
對應至使用者事件結束事件的值。 未使用。

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET \_ USERMARKER**  
對應至使用者標記事件的值。

<span id="ET_CALL"></span><span id="et_call"></span>**ET \_ 呼叫**  
對應至呼叫事件的值。

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ OBJECTCREATION**  
對應至物件建立事件的值。

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ OBJECTPOPULATION**  
對應至物件人口事件的值。

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ CALLSYNC**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**ET \_ 繪圖**  
對應至繪製呼叫事件的值。

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET \_ 分派**  
對應至分派事件的值。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>
