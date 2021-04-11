---
title: 方向 (參數) 屬性
description: 方向屬性描述資料是從用戶端傳送到伺服器、伺服器到用戶端，還是從兩者傳送。
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- 遠端程序呼叫 RPC、描述的方向屬性
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092948"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="5a4a2-106">方向 (參數) 屬性</span><span class="sxs-lookup"><span data-stu-id="5a4a2-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="5a4a2-107">方向屬性描述資料是從用戶端傳送到伺服器、伺服器到用戶端，還是從兩者傳送。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="5a4a2-108">函數原型中的所有參數都必須與方向屬性相關聯。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="5a4a2-109">有三種可能的方向屬性組合： 1) \[ [**in**](/windows/desktop/Midl/in)、 \] 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] 和 3) \[ **in**、 **out** \] 。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="5a4a2-110">這些描述在呼叫和呼叫程式之間傳遞參數的方式。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="5a4a2-111">當您在預設的 (Microsoft 擴充模式) 中進行編譯時，會省略參數的方向屬性，MIDL 編譯器會假設的預設值為 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="5a4a2-112">\[ [**Out**](/windows/desktop/Midl/out-idl) \] 參數必須是指標。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="5a4a2-113">事實上， \[  \] 因為 C 函式參數是以傳值方式傳遞，所以 out 屬性在套用至不做為指標的參數時沒有意義。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="5a4a2-114">在 C 中，被呼叫的函式會收到參數值的私用複本。它無法變更該參數的呼叫函數值。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="5a4a2-115">但是，如果參數做為指標，則可以用來存取和修改記憶體。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="5a4a2-116">\[ **Out** \] 屬性工作表示伺服器函式應該將值傳回給用戶端的呼叫函式，而且應該根據指派給指標的屬性，傳回與指標相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="5a4a2-117">下列介面示範三種可能適用于參數的方向屬性組合。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="5a4a2-118">函數 **InOutProc** 定義于 IDL 檔案中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5a4a2-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="5a4a2-119">第一個參數 *s1* 是唯一的 \[ [](/windows/desktop/Midl/in) \] 。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="5a4a2-120">它的值會傳送到遠端電腦，但不會傳回給呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="5a4a2-121">雖然伺服器應用程式可以變更 *s1* 的值，但用戶端上的 *s1* 值在呼叫前後都相同。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="5a4a2-122">第二個參數（ *ps2*）在函式原型中定義為具有 \[ [**in**](/windows/desktop/Midl/in) \] 和 \[ [**out**](/windows/desktop/Midl/out-idl) \] 屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="5a4a2-123">\[ **In** \] 屬性工作表示參數的值會從用戶端傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="5a4a2-124">\[ **Out** \] 屬性工作表示 *ps2* 所指向的值會傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="5a4a2-125">第三個參數 \[ 只是 [**out**](/windows/desktop/Midl/out-idl) \] 。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="5a4a2-126">在伺服器上配置參數的空間，但輸入時未定義此值。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="5a4a2-127">如先前所述，所有 \[ **out** \] 參數都必須是指標。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="5a4a2-128">遠端程式會變更這三個參數的值，但只有 \[ [**out**](/windows/desktop/Midl/out-idl) \] 和 in 參數的新值 \[ [](/windows/desktop/Midl/in) \] 可供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="5a4a2-129">從呼叫 **InOutProc** 時，會修改第二個和第三個參數。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="5a4a2-130">第一個參數（唯一的參數） \[ [](/windows/desktop/Midl/in) \] 不會變更。</span><span class="sxs-lookup"><span data-stu-id="5a4a2-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![in 參數](images/prog-a22.png)

![out 參數](images/prog-a23.png)

![out 參數](images/prog-a21.png)

 

 