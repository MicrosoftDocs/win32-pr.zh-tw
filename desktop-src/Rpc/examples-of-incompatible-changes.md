---
title: 不相容變更的範例
description: 在處理不相容的變更時，不幸的經驗法則如下：任何變更都可以回溯不相容，除非它很清楚地瞭解。
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021603"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="a310e-103">不相容變更的範例</span><span class="sxs-lookup"><span data-stu-id="a310e-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="a310e-104">處理不相容的變更時，很不幸的經驗法則如下：任何變更都可以回溯不相容，除非它已經過充分瞭解。</span><span class="sxs-lookup"><span data-stu-id="a310e-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="a310e-105">這項規則需要瞭解 NDR 規則。</span><span class="sxs-lookup"><span data-stu-id="a310e-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="a310e-106">如果您不知道 NDR 是什麼，請勿進行修改。</span><span class="sxs-lookup"><span data-stu-id="a310e-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="a310e-107">通常會導致應用程式發生存取違規的變更範例，或是 \_ \_ \_ 封送處理引擎引發的錯誤存根資料例外狀況，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a310e-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="a310e-108">將新方法加入舊方法的中間。</span><span class="sxs-lookup"><span data-stu-id="a310e-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="a310e-109">從方法新增或移除參數。</span><span class="sxs-lookup"><span data-stu-id="a310e-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="a310e-110">變更屬性，例如指標屬性：將 \[ ref 變更 \] 為 \[ unique \] 或 ptr， \[ 反之亦然 \] 。</span><span class="sxs-lookup"><span data-stu-id="a310e-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="a310e-111">每個指標類型都有不同的網路標記法。</span><span class="sxs-lookup"><span data-stu-id="a310e-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="a310e-112">變更資料的大小：從短到長、從 char 到 wchar \_ t (unicode) 、將欄位加入至結構，以及變更固定大小陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="a310e-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="a310e-113">使用 default 子句將聯集臂加入至聯集。</span><span class="sxs-lookup"><span data-stu-id="a310e-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="a310e-114">用戶端與伺服器之間的部分應變變更或非預期的不符，可能會如下所示：</span><span class="sxs-lookup"><span data-stu-id="a310e-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="a310e-115">修改複合類型的成員，例如結構或陣列。</span><span class="sxs-lookup"><span data-stu-id="a310e-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="a310e-116">例如，如果用戶端 \_ 識別碼從整數變更為 GUID，用戶端識別碼欄位的用戶端 \_ 記錄結構 \_ 就會變成不相容。</span><span class="sxs-lookup"><span data-stu-id="a310e-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="a310e-117">如果透過數個內嵌層級，將其設為實際的遠端參數類型，則可能很難偵測到此情況。</span><span class="sxs-lookup"><span data-stu-id="a310e-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="a310e-118">修改匯入的類型。</span><span class="sxs-lookup"><span data-stu-id="a310e-118">Modifying an imported type.</span></span> <span data-ttu-id="a310e-119">類型可能來自不同的元件，而不會直接從遠端執行，因此會將變更視為相容。</span><span class="sxs-lookup"><span data-stu-id="a310e-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="a310e-120">在 IDL 檔案中使用 \# ifdef 對於 idl 檔案中的 ifdef 型別定義而言是不好的概念，因為這會造成損毀的等候發生。</span><span class="sxs-lookup"><span data-stu-id="a310e-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="a310e-121">不可避免的，由於組建或其他問題，用戶端會使用一組不同的定義來進行編譯，而這些定義的定義與伺服器不同，最後就是不相容的。</span><span class="sxs-lookup"><span data-stu-id="a310e-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




