---
title: 移植鳶尾花 GL Get 函數
description: 鳶尾花 GL \ 0034; get \ 0034;函數採用下列形式
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- 鳶尾花 GL 移植，取得函式
- 從鳶尾花 GL 進行移植，取得函數
- 從鳶尾花 GL 移植至 OpenGL，取得函數
- 從鳶尾花 GL 進行 OpenGL 移植，取得函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfe9159e0207198fa94959729bd0c95439bb91b5dd55a8a1f9adf3b048d7bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485558"
---
# <a name="porting-iris-gl-get-functions"></a>移植鳶尾花 GL Get 函數

鳶尾花 GL "get" 函式採用下列格式：

``` syntax
int getthing();
```

及

``` syntax
int getthings( int *a, int *b);
```

您的鳶尾花 GL 程式碼可能包含如下所示的 get 函式呼叫：

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

在 OpenGL 中，您可以使用下列四種類型的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 函式之一來取代相等的鳶尾花 GL get 函式：

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

這些函數具有下列語法：

``` syntax
glGet<Datatype>v( value, *data );
```

其中 *值* 的型別為 **GLenum** ，而資料的型別為 **GLdatatype**。 當您呼叫 **glGet** 時，它會傳回與預期型別不同的類型，類型會適當地進行轉換。 如需 **glGet** 參數的完整清單，請參閱 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)。

 

 




