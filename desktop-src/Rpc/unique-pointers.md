---
title: 唯一指標
description: 在 C 程式中，有一個以上的指標可以包含資料的位址。
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023512"
---
# <a name="unique-pointers"></a><span data-ttu-id="295b6-103">唯一指標</span><span class="sxs-lookup"><span data-stu-id="295b6-103">Unique Pointers</span></span>

<span data-ttu-id="295b6-104">在 C 程式中，有一個以上的指標可以包含資料的位址。</span><span class="sxs-lookup"><span data-stu-id="295b6-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="295b6-105">指標稱為建立資料的 [*別名*](a-glos.md) 。</span><span class="sxs-lookup"><span data-stu-id="295b6-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="295b6-106">當指標指向宣告的變數時，也會建立別名。</span><span class="sxs-lookup"><span data-stu-id="295b6-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="295b6-107">下列程式碼片段說明這兩種別名方法：</span><span class="sxs-lookup"><span data-stu-id="295b6-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="295b6-108">在典型的 C 程式中，您可以使用下列定義來指定二進位樹狀結構：</span><span class="sxs-lookup"><span data-stu-id="295b6-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="295b6-109">有一個以上的指標可以存取樹狀節點的內容。</span><span class="sxs-lookup"><span data-stu-id="295b6-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="295b6-110">這通常適用于非分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="295b6-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="295b6-111">不過，這種程式設計樣式會產生更複雜的 RPC 支援程式碼。</span><span class="sxs-lookup"><span data-stu-id="295b6-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="295b6-112">用戶端和伺服器 stub 需要額外的程式碼來管理資料和指標。</span><span class="sxs-lookup"><span data-stu-id="295b6-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="295b6-113">基礎存根程式碼必須解析位址的各種指標，並判斷哪一個資料複本代表最新版本。</span><span class="sxs-lookup"><span data-stu-id="295b6-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="295b6-114">如果您保證指標是應用程式可以存取該記憶體區域的唯一方法，就可以減少處理量。</span><span class="sxs-lookup"><span data-stu-id="295b6-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="295b6-115">指標仍可具有 C 指標的許多功能。</span><span class="sxs-lookup"><span data-stu-id="295b6-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="295b6-116">例如，它可以在 **null** 和非 **null** 值之間變更或保持不變。</span><span class="sxs-lookup"><span data-stu-id="295b6-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="295b6-117">下列範例將說明這點。</span><span class="sxs-lookup"><span data-stu-id="295b6-117">The following example illustrates this.</span></span> <span data-ttu-id="295b6-118">指標在呼叫之前為 **null** ，並指向呼叫之後的有效字串：</span><span class="sxs-lookup"><span data-stu-id="295b6-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![在 null 和非 null 值之間變更指標](images/prog-a01.png)

<span data-ttu-id="295b6-120">根據預設，MIDL 編譯器會將 \[ [唯一](/windows/desktop/Midl/unique) \] 指標屬性套用至並非參數的所有指標。</span><span class="sxs-lookup"><span data-stu-id="295b6-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="295b6-121">您可以使用 \[ [指標 \_ 預設](/windows/desktop/Midl/pointer-default)屬性來變更此預設設定 \] 。</span><span class="sxs-lookup"><span data-stu-id="295b6-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="295b6-122">唯一指標具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="295b6-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="295b6-123">其值可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="295b6-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="295b6-124">在呼叫期間，它可以從 **null** 變更為非 **null** 。</span><span class="sxs-lookup"><span data-stu-id="295b6-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="295b6-125">當值變更為非 **null** 時，會在傳回時配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="295b6-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="295b6-126">在呼叫期間，它可以從非 **null** 變更為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="295b6-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="295b6-127">當值變更為 **Null** 時，應用程式會負責釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="295b6-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="295b6-128">值可以從一個非 **null** 值變更為另一個值。</span><span class="sxs-lookup"><span data-stu-id="295b6-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="295b6-129">唯一指標指向的儲存區無法由作業中的任何其他指標或名稱存取。</span><span class="sxs-lookup"><span data-stu-id="295b6-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="295b6-130">如果指標沒有 **null** 值，則會將傳回的資料寫入至現有的儲存體。</span><span class="sxs-lookup"><span data-stu-id="295b6-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="295b6-131">下列範例示範如何定義唯一指標。</span><span class="sxs-lookup"><span data-stu-id="295b6-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="295b6-132">在此範例中，參數 *ach* 是傳送至伺服器以使用 RemoteFn 常式處理的字元資料的唯一指標。</span><span class="sxs-lookup"><span data-stu-id="295b6-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 