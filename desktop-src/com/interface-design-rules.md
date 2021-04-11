---
title: 介面設計規則
description: 本節提供介面設計規則和指導方針的簡短摘要。
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093343"
---
# <a name="interface-design-rules"></a><span data-ttu-id="c080c-103">介面設計規則</span><span class="sxs-lookup"><span data-stu-id="c080c-103">Interface Design Rules</span></span>

<span data-ttu-id="c080c-104">本節提供介面設計規則和指導方針的簡短摘要。</span><span class="sxs-lookup"><span data-stu-id="c080c-104">This section provides a short summary of interface design rules and guidelines.</span></span> <span data-ttu-id="c080c-105">其中有些規則是 COM 架構特有的，有些則是介面設計語言（MIDL）所加諸的限制。</span><span class="sxs-lookup"><span data-stu-id="c080c-105">Some of these rules are specific to the COM architecture, while others are restrictions imposed by the interface design language, MIDL.</span></span> <span data-ttu-id="c080c-106">如需 COM 介面設計的詳細資訊，請參閱 [IDL 檔案的剖析](anatomy-of-an-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="c080c-106">For details of COM interface design, see [Anatomy of an IDL File](anatomy-of-an-idl-file.md).</span></span>

<span data-ttu-id="c080c-107">根據定義，物件不是 COM 物件，除非它會執行 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面或衍生自 **iunknown** 的介面。</span><span class="sxs-lookup"><span data-stu-id="c080c-107">By definition, an object is not a COM object unless it implements either the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface or an interface that is derived from **IUnknown**.</span></span> <span data-ttu-id="c080c-108">此外，下列規則適用于 COM 物件上所執行的所有介面：</span><span class="sxs-lookup"><span data-stu-id="c080c-108">In addition, the following rules apply to all interfaces implemented on a COM object:</span></span>

-   <span data-ttu-id="c080c-109">它們必須有唯一的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="c080c-109">They must have a unique interface identifier (IID).</span></span>
-   <span data-ttu-id="c080c-110">它們必須是不可變的。</span><span class="sxs-lookup"><span data-stu-id="c080c-110">They must be immutable.</span></span> <span data-ttu-id="c080c-111">一旦建立併發布之後，其定義的任何部分都不會變更。</span><span class="sxs-lookup"><span data-stu-id="c080c-111">Once they are created and published, no part of their definition may change.</span></span>
-   <span data-ttu-id="c080c-112">所有介面方法都必須傳回 **HRESULT** 值，讓處理遠端處理的系統部分可以回報 RPC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c080c-112">All interface methods must return an **HRESULT** value so that the portions of the system that handle remote processing can report RPC errors.</span></span>
-   <span data-ttu-id="c080c-113">介面方法中的所有字串參數都必須是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="c080c-113">All string parameters in interface methods must be Unicode.</span></span>
-   <span data-ttu-id="c080c-114">您的資料類型必須可以遠端處理。</span><span class="sxs-lookup"><span data-stu-id="c080c-114">Your data types must be remotable.</span></span> <span data-ttu-id="c080c-115">如果您無法將資料類型轉換成可遠端處理的型別，就必須建立自己的封送處理和封送處理常式。</span><span class="sxs-lookup"><span data-stu-id="c080c-115">If you cannot convert a data type to a remotable type, you will have to create your own marshaling and unmarshaling routines.</span></span> <span data-ttu-id="c080c-116">此外， **LPVOID** 或 **void \*** 在遠端電腦上沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c080c-116">Also, **LPVOID**, or **void \***, has no meaning on a remote computer.</span></span> <span data-ttu-id="c080c-117">如有必要，請使用 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的指標。</span><span class="sxs-lookup"><span data-stu-id="c080c-117">Use a pointer to [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="c080c-118">MIDL 的目前執行不會處理函數多載或多重繼承。</span><span class="sxs-lookup"><span data-stu-id="c080c-118">The current implementation of MIDL does not handle function overloading or multiple inheritance.</span></span>

 

## <a name="other-interface-design-considerations"></a><span data-ttu-id="c080c-119">其他介面設計考慮</span><span class="sxs-lookup"><span data-stu-id="c080c-119">Other Interface Design Considerations</span></span>

<span data-ttu-id="c080c-120">非常小心地使用資料指標。</span><span class="sxs-lookup"><span data-stu-id="c080c-120">Use pointers to data very carefully.</span></span> <span data-ttu-id="c080c-121">若要在呼叫之進程的位址空間中重新建立資料，RPC 執行時間必須知道資料的確切大小。</span><span class="sxs-lookup"><span data-stu-id="c080c-121">To re-create the data in the address space of the process that is called, the RPC run time must know the exact size of the data.</span></span> <span data-ttu-id="c080c-122">例如，如果 **CHAR \*** 參數指向字元緩衝區，而不是單一字元，則無法正確地重新建立資料。</span><span class="sxs-lookup"><span data-stu-id="c080c-122">If, for example, a **CHAR \*** parameter points to a buffer of characters rather than to a single character, the data cannot be correctly re-created.</span></span> <span data-ttu-id="c080c-123">使用 MIDL 提供的語法，準確地描述您的型別定義所代表的資料結構。</span><span class="sxs-lookup"><span data-stu-id="c080c-123">Use the syntax available with MIDL to accurately describe the data structures represented by your type definitions.</span></span>

<span data-ttu-id="c080c-124">針對內嵌于陣列和結構並跨進程界限傳遞的指標，初始化是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="c080c-124">Initialization is essential for pointers that are embedded in arrays and structures and passed across process boundaries.</span></span> <span data-ttu-id="c080c-125">未初始化的指標在傳遞至相同進程空間中的程式時可能會運作，但 proxy 和存根會假設所有指標都使用有效的位址初始化，或為 null。</span><span class="sxs-lookup"><span data-stu-id="c080c-125">Uninitialized pointers may work when passed to a program in the same process space, but proxies and stubs assume that all pointers are initialized with valid addresses or are null.</span></span>

<span data-ttu-id="c080c-126">當別名指標 (允許指標指向相同的記憶體) 部分時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="c080c-126">Be careful when aliasing pointers (allowing pointers to point to the same piece of memory).</span></span> <span data-ttu-id="c080c-127">如果別名是故意的，則這些指標應該在 IDL 檔案中宣告為別名。</span><span class="sxs-lookup"><span data-stu-id="c080c-127">If the aliasing is intentional, these pointers should be declared aliased in the IDL file.</span></span> <span data-ttu-id="c080c-128">宣告為 nonaliased 的指標絕對不能有別名。</span><span class="sxs-lookup"><span data-stu-id="c080c-128">Pointers declared as nonaliased should never alias each other.</span></span>

<span data-ttu-id="c080c-129">請注意您如何配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="c080c-129">Pay attention to how you allocate and free memory.</span></span> <span data-ttu-id="c080c-130">請記住，除非您使用 [ [**配置**](/windows/desktop/Midl/allocate) ] 屬性明確地告知 COM 物件 () 不要釋放跨進程調用期間所建立的資料結構，否則該結構將在呼叫完成時終結。</span><span class="sxs-lookup"><span data-stu-id="c080c-130">Remember that, unless you explicitly tell a COM object (by using the [**allocate**](/windows/desktop/Midl/allocate) attribute) not to free a data structure that was created during an out-of-process call, that structure will be destroyed when the call completes.</span></span> <span data-ttu-id="c080c-131">此外，請考慮可能會造成破壞性的資料結構配置所建立的破壞性額外負荷，現在需要封送處理和取消封送處理。</span><span class="sxs-lookup"><span data-stu-id="c080c-131">Also, consider the potentially destructive overhead created by inefficient allocation of data structures that now need to be marshaled and unmarshaled.</span></span>

<span data-ttu-id="c080c-132">最後，定義 **HRESULT** 傳回值時請務必小心，如此一來，您就不會建立與 COM 定義的設備 ITF 程式碼衝突的錯誤碼， \_ (0x0000 和0x01FF 之間的值會保留) 或與具有相同值的其他 **HRESULT** 值發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c080c-132">Finally, be careful when defining your **HRESULT** return values so that you don't create error codes that conflict with COM-defined FACILITY\_ITF codes (values between 0x0000 and 0x01FF are reserved) or that conflict with other **HRESULT** values with the same value.</span></span> <span data-ttu-id="c080c-133">可能的話，請使用通用 COM 成功和失敗傳回值，並使用 [**out**](/windows/desktop/Midl/out-idl) 參數（而非 **HRESULT**）來傳回函式呼叫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="c080c-133">Whenever possible, use the universal COM success and failure return values, and use an [**out**](/windows/desktop/Midl/out-idl) parameter, rather than an **HRESULT**, to return information specific to the function call.</span></span>

<span data-ttu-id="c080c-134">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c080c-134">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c080c-135">設計可遠端處理的介面</span><span class="sxs-lookup"><span data-stu-id="c080c-135">Designing Remotable Interfaces</span></span>](designing-remotable-interfaces.md)
-   [<span data-ttu-id="c080c-136">使用 COM 介面</span><span class="sxs-lookup"><span data-stu-id="c080c-136">Using a COM Interface</span></span>](using-a-com-interface.md)

## <a name="related-topics"></a><span data-ttu-id="c080c-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="c080c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c080c-138">介面定義和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="c080c-138">Interface Definitions and Type Libraries</span></span>](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 