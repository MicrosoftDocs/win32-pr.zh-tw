---
title: 定義 COM 介面
description: Microsoft 會定義許多 COM 介面。 在大多數情況下，您可以重複使用這些泛型介面。 不過，有些應用程式有特定需求，因此需要或需要定義您自己的物件介面。
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093360"
---
# <a name="defining-com-interfaces"></a><span data-ttu-id="284c7-105">定義 COM 介面</span><span class="sxs-lookup"><span data-stu-id="284c7-105">Defining COM Interfaces</span></span>

<span data-ttu-id="284c7-106">Microsoft 會定義許多 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="284c7-106">Microsoft defines many COM interfaces.</span></span> <span data-ttu-id="284c7-107">在大多數情況下，您可以重複使用這些泛型介面。</span><span class="sxs-lookup"><span data-stu-id="284c7-107">In most cases, you can reuse these generic interfaces.</span></span> <span data-ttu-id="284c7-108">不過，有些應用程式有特定需求，因此需要或需要定義您自己的物件介面。</span><span class="sxs-lookup"><span data-stu-id="284c7-108">However, some applications have specific requirements that make it desirable or necessary to define your own object interfaces.</span></span>

<span data-ttu-id="284c7-109">所有 COM 介面都必須直接或間接衍生自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="284c7-109">All COM interfaces must derive, directly or indirectly, from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="284c7-110">在該條件約束內，您的自訂介面幾乎可以支援任何方法或參數，包括非同步方法。</span><span class="sxs-lookup"><span data-stu-id="284c7-110">Within that constraint, your custom interface can support almost any method or parameter, including asynchronous methods.</span></span> <span data-ttu-id="284c7-111">您也可以為自訂介面產生類型程式庫，讓用戶端可以在執行時間存取物件方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="284c7-111">You can also generate a type library for your custom interfaces so that clients can access information about your object's methods at run time.</span></span> <span data-ttu-id="284c7-112">在您定義介面之後，請使用 Microsoft 介面定義語言 (MIDL) 來加以描述、編譯並註冊它，就像使用任何泛型介面一樣。</span><span class="sxs-lookup"><span data-stu-id="284c7-112">After you define an interface, describe it in Microsoft Interface Definition Language (MIDL), compile and register it, you use it just like any generic interface.</span></span> <span data-ttu-id="284c7-113">使用分散式 COM 時，介面方法可用於遠端進程以及相同電腦上的其他進程。</span><span class="sxs-lookup"><span data-stu-id="284c7-113">With distributed COM, interface methods are available both to remote processes and to other processes on the same computer.</span></span>

<span data-ttu-id="284c7-114">最後，建立 COM 介面需要一個包含 C/c + + 編譯器和 Midl.exe 編譯器的開發環境。</span><span class="sxs-lookup"><span data-stu-id="284c7-114">Finally, building COM interfaces requires a development environment that includes a C/C++ compiler and the Midl.exe compiler.</span></span>

<span data-ttu-id="284c7-115">建立 COM 介面的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="284c7-115">The steps in creating a COM interface are as follows:</span></span>

-   <span data-ttu-id="284c7-116">決定您要如何為您的介面提供封送處理支援;使用類型程式庫驅動封送處理，或使用 proxy/stub DLL。</span><span class="sxs-lookup"><span data-stu-id="284c7-116">Decide how you want to provide marshaling support for your interface; either with type-library driven marshaling or with a proxy/stub DLL.</span></span> <span data-ttu-id="284c7-117">即使同進程介面要跨多個範圍界限使用，也必須封送處理。</span><span class="sxs-lookup"><span data-stu-id="284c7-117">Even in-process interfaces must be marshaled if they are to be used across apartment boundaries.</span></span> <span data-ttu-id="284c7-118">最好是將封送處理支援建立至每個 COM 介面，即使您不認為您將需要它。</span><span class="sxs-lookup"><span data-stu-id="284c7-118">It is a good idea to build marshaling support into every COM interface, even if you don't think you will need it.</span></span> <span data-ttu-id="284c7-119">如需詳細資訊，請參閱 [介面封送處理](interface-marshaling.md) 。</span><span class="sxs-lookup"><span data-stu-id="284c7-119">See [Interface Marshaling](interface-marshaling.md) for more information.</span></span>
-   <span data-ttu-id="284c7-120">描述介面定義中的介面或介面 (IDL) 檔。</span><span class="sxs-lookup"><span data-stu-id="284c7-120">Describe the interface or interfaces in an interface definition (IDL) file.</span></span> <span data-ttu-id="284c7-121">此外，您可以在應用程式佈建檔中指定介面的特定本機層面 (ACF) 。</span><span class="sxs-lookup"><span data-stu-id="284c7-121">In addition, you can specify certain local aspects of your interface in an application configuration file (ACF).</span></span> <span data-ttu-id="284c7-122">如果您使用類型程式庫驅動封送處理，請新增連結 [**庫**](/windows/desktop/Midl/library) 語句，以參考您要產生類型資訊的介面。</span><span class="sxs-lookup"><span data-stu-id="284c7-122">If you are using type-library driven marshaling, add a [**library**](/windows/desktop/Midl/library) statement that references the interfaces for which you want to generate type information.</span></span>
-   <span data-ttu-id="284c7-123">使用 MIDL 編譯器來產生類型程式庫檔案和標頭檔案，或 C 語言 proxy/stub 檔案、介面識別碼檔案、DLL 資料檔案和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="284c7-123">Use the MIDL compiler to generate a type library file and header file, or C-language proxy/stub files, interface identifier file, DLL data file and header file.</span></span> <span data-ttu-id="284c7-124">如需詳細資訊，請參閱 [MIDL 編譯](midl-compilation.md) 。</span><span class="sxs-lookup"><span data-stu-id="284c7-124">See [MIDL Compilation](midl-compilation.md) for more information.</span></span>
-   <span data-ttu-id="284c7-125">根據您選擇的封送處理方法，將模組定義寫入 (DEF) 檔案、將所有 MIDL 產生的檔案編譯並連結到單一 proxy DLL 中，並在系統登錄中註冊介面，或註冊類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="284c7-125">Depending on the marshaling method you chose, write a module definition (DEF) file, compile and link all the MIDL-generated files into a single proxy DLL, and register the interface in the system registry, or register the type library.</span></span> <span data-ttu-id="284c7-126">如需詳細資訊，請參閱 [載入和註冊類型程式庫](loading-and-registering-a-type-library.md) ，以及 [建立和註冊 Proxy DLL](building-and-registering-a-proxy-dll.md) 。</span><span class="sxs-lookup"><span data-stu-id="284c7-126">See [Loading and Registering a Type Library](loading-and-registering-a-type-library.md) and [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="284c7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="284c7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="284c7-128">IDL 檔案的剖析</span><span class="sxs-lookup"><span data-stu-id="284c7-128">Anatomy of an IDL File</span></span>](anatomy-of-an-idl-file.md)
</dt> <dt>

[<span data-ttu-id="284c7-129">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="284c7-129">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="284c7-130">介面設計規則</span><span class="sxs-lookup"><span data-stu-id="284c7-130">Interface Design Rules</span></span>](interface-design-rules.md)
</dt> <dt>

[<span data-ttu-id="284c7-131">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="284c7-131">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 