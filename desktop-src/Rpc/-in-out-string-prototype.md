---
title: " in、out、string 原型"
description: 下列函式原型針對輸入和輸出字串使用單一的 in、out、string \ 參數。
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933344"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="640c6-103">\[in、out、string \] 原型</span><span class="sxs-lookup"><span data-stu-id="640c6-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="640c6-104">下列函式原型 \[ [](/windows/desktop/Midl/in)針對輸入和輸出字串使用單一 in、 [**out**](/windows/desktop/Midl/out-idl)、 [**string**](/windows/desktop/Midl/string) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="640c6-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="640c6-105">字串首先包含患者輸入，然後以醫生回應覆寫，如下所示：</span><span class="sxs-lookup"><span data-stu-id="640c6-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="640c6-106">這個範例類似于針對輸入和輸出採用單一計數位符串的範例。</span><span class="sxs-lookup"><span data-stu-id="640c6-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="640c6-107">就像這樣的範例一樣， \[ [**size \_ 是**](/windows/desktop/Midl/size-is)屬性（attribute）會 \] 決定伺服器上配置的元素數目。</span><span class="sxs-lookup"><span data-stu-id="640c6-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="640c6-108">\[[**字串**](/windows/desktop/Midl/string) \] 屬性會指示存根呼叫 **strlen** ，以判斷已傳送的元素數目。</span><span class="sxs-lookup"><span data-stu-id="640c6-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="640c6-109">用戶端會在呼叫之前配置所有的記憶體，如下所示：</span><span class="sxs-lookup"><span data-stu-id="640c6-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="640c6-110">請注意，[分析] 函數不再需要計算傳回字串的長度，就如同在未使用 **\[ 字串 \]** 屬性的計數位符串範例中所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="640c6-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="640c6-111">現在，存根會計算如下所示的長度：</span><span class="sxs-lookup"><span data-stu-id="640c6-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 