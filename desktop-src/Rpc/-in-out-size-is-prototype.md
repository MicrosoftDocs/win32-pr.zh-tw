---
title: " in、out、size_is 原型"
description: '\ in、out、size \_ 是 \ 原型使用從用戶端到伺服器，以及從伺服器傳遞至用戶端的單一計數位符陣列。'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623dc39e9bd18fdd0c7bc02f008ccc1c16919362fd2a52e373abdde762eb726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073638"
---
# <a name="in-out-size_is-prototype"></a>\[in、out、size \_ 為 \] 原型

下列函式原型使用以兩種方式傳遞的單一計數位符陣列：從用戶端到伺服器，以及從伺服器到用戶端：

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

\[ [](/windows/desktop/Midl/in) \] *AchInOut* 必須指向用戶端上的有效儲存體，做為 in 參數。 開發人員在進行遠端程序呼叫之前，會先在用戶端上配置與陣列相關聯的記憶體。

存根使用的 \[ [**大小 \_ 是**](/windows/desktop/Midl/size-is) \] 參數 *strsize* 來佈建服務器上的記憶體，然後使用 \[ [**長度 \_ 為**](/windows/desktop/Midl/length-is) \] 參數 *pcbSize* ，將陣列元素傳輸至此記憶體。 開發人員必須確定用戶端程式代碼會在呼叫遠端程式之前，先將 **\[ 長度設定 \_ 為 \]** 變數。

在某些情況下，針對輸入和輸出使用不同的參數，而不是單一字串，會更有效率，並提供彈性。 下一個範例會示範這一點：

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

在上述範例中，字元陣列 achInOut 也用來當做 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。 在 C 中，陣列的名稱相當於使用指標。 依預設，所有最上層指標都是參考指標，它們在值中不會變更，而且會在呼叫前後指向用戶端上相同的記憶體區域。 遠端程式所存取的所有記憶體都必須符合用戶端在呼叫之前指定的大小，否則 stub 將會產生例外狀況。

在傳回之前，伺服器上的分析函數必須重設 *pcbSize* 參數，以指出伺服器將傳送至用戶端的元素數目，如下所示：

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 