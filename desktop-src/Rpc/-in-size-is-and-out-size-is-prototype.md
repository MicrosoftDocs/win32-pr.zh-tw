---
title: " in、size_is 和 out size_is 原型"
description: 下列函式原型會使用兩個計數位符串。 開發人員必須在用戶端和伺服器上撰寫程式碼，以追蹤字元陣列長度，並傳遞參數來告訴存根要傳輸多少陣列元素。
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382622"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[在中，大小 \_ 為 \] 和 \[ 輸出，大小 \_ 為 \] 原型

下列函式原型會使用兩個計數位符串。 開發人員必須在用戶端和伺服器上撰寫程式碼，以追蹤字元陣列長度，並傳遞參數來告訴存根要傳輸多少陣列元素。

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

請注意，描述陣列長度的參數會以和陣列相同的方向傳送： *cbIn* 和 *achIn* 是 \[ [**In**](/windows/desktop/Midl/in) \] 參數，而 *pcbOut* 和 *achOut* 是 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。 作為 **\[ \] out** 參數，參數 *pcbOut* 必須遵循 C 慣例，並宣告為指標。

在呼叫遠端程式之前，用戶端程式代碼會計算字串中的字元數（包括尾端零），如下所示：

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

伺服器上的遠端程式會在 *cbOut* 中提供傳回緩衝區的長度，如下所示：

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

\[  \] 當參數已知為字串時，就可以使用字串屬性。 此屬性會指示存根來計算字串大小，藉此排除與長度相關聯的額外負荷 \[ [**為**](/windows/desktop/Midl/size-is) \] 參數。 此外，它會指示存根在將參數傳遞至應用程式之前，先確認字串是否為 **Null** 終止。

 

 