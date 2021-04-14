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
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="34eaf-104">\[在中，大小 \_ 為 \] 和 \[ 輸出，大小 \_ 為 \] 原型</span><span class="sxs-lookup"><span data-stu-id="34eaf-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="34eaf-105">下列函式原型會使用兩個計數位符串。</span><span class="sxs-lookup"><span data-stu-id="34eaf-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="34eaf-106">開發人員必須在用戶端和伺服器上撰寫程式碼，以追蹤字元陣列長度，並傳遞參數來告訴存根要傳輸多少陣列元素。</span><span class="sxs-lookup"><span data-stu-id="34eaf-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="34eaf-107">請注意，描述陣列長度的參數會以和陣列相同的方向傳送： *cbIn* 和 *achIn* 是 \[ [**In**](/windows/desktop/Midl/in) \] 參數，而 *pcbOut* 和 *achOut* 是 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="34eaf-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="34eaf-108">作為 **\[ \] out** 參數，參數 *pcbOut* 必須遵循 C 慣例，並宣告為指標。</span><span class="sxs-lookup"><span data-stu-id="34eaf-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="34eaf-109">在呼叫遠端程式之前，用戶端程式代碼會計算字串中的字元數（包括尾端零），如下所示：</span><span class="sxs-lookup"><span data-stu-id="34eaf-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="34eaf-110">伺服器上的遠端程式會在 *cbOut* 中提供傳回緩衝區的長度，如下所示：</span><span class="sxs-lookup"><span data-stu-id="34eaf-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

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

<span data-ttu-id="34eaf-111">\[  \] 當參數已知為字串時，就可以使用字串屬性。</span><span class="sxs-lookup"><span data-stu-id="34eaf-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="34eaf-112">此屬性會指示存根來計算字串大小，藉此排除與長度相關聯的額外負荷 \[ [**為**](/windows/desktop/Midl/size-is) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="34eaf-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="34eaf-113">此外，它會指示存根在將參數傳遞至應用程式之前，先確認字串是否為 **Null** 終止。</span><span class="sxs-lookup"><span data-stu-id="34eaf-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 