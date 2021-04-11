---
title: COM、DCOM 和型別程式庫
description: 元件物件模型 (COM) 和分散式元件物件模型 (DCOM) 使用遠端程序呼叫 (RPC) ，讓分散式元件物件能夠彼此通訊。
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- 介面 MIDL、COM
- 介面 MIDL、DCOM
- 介面 MIDL、類型程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842220"
---
# <a name="com-dcom-and-type-libraries"></a><span data-ttu-id="df3ff-106">COM、DCOM 和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="df3ff-106">COM, DCOM, and Type Libraries</span></span>

<span data-ttu-id="df3ff-107">元件物件模型 (COM) 和分散式元件物件模型 (DCOM) 使用遠端程序呼叫 (RPC) ，讓分散式元件物件能夠彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="df3ff-107">Component Object Model (COM) and Distributed Component Object Model (DCOM) use Remote Procedure Calls (RPC) to enable distributed component objects to communicate with each other.</span></span> <span data-ttu-id="df3ff-108">因此，COM 或 DCOM 介面會定義 COM 物件的身分識別和外部特性。</span><span class="sxs-lookup"><span data-stu-id="df3ff-108">Thus, a COM or DCOM interface defines the identity and external characteristics of a COM object.</span></span> <span data-ttu-id="df3ff-109">它會形成用戶端存取物件方法和資料的方式。</span><span class="sxs-lookup"><span data-stu-id="df3ff-109">It forms the means by which clients can gain access to an object's methods and data.</span></span> <span data-ttu-id="df3ff-110">使用 DCOM，不論物件是否存在於相同的進程中、相同電腦上的不同進程，或不同的電腦上，都可以存取此存取。</span><span class="sxs-lookup"><span data-stu-id="df3ff-110">With DCOM, this access is possible regardless of whether the objects exist in the same process, different processes on the same machine, or on different machines.</span></span> <span data-ttu-id="df3ff-111">如同 RPC 用戶端/伺服器介面，COM 或 DCOM 物件可以透過數種不同的方式和多個介面來公開其功能。</span><span class="sxs-lookup"><span data-stu-id="df3ff-111">As with RPC client/server interfaces, a COM or DCOM object can expose its functionality in a number of different ways and through multiple interfaces.</span></span>

## <a name="type-library"></a><span data-ttu-id="df3ff-112">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df3ff-112">Type Library</span></span>

<span data-ttu-id="df3ff-113">類型程式庫 ( .tlb) 是一種二進位檔案，它會將 COM 或 DCOM 物件的屬性和方法的相關資訊儲存在執行時間可供其他應用程式存取的表單中。</span><span class="sxs-lookup"><span data-stu-id="df3ff-113">A type library (.tlb) is a binary file that stores information about a COM or DCOM object's properties and methods in a form that is accessible to other applications at runtime.</span></span> <span data-ttu-id="df3ff-114">使用類型程式庫，應用程式或瀏覽器可以判斷物件支援的介面，以及叫用物件的介面方法。</span><span class="sxs-lookup"><span data-stu-id="df3ff-114">Using a type library, an application or browser can determine which interfaces an object supports, and invoke an object's interface methods.</span></span> <span data-ttu-id="df3ff-115">即使物件和用戶端應用程式是以不同的程式設計語言撰寫，也可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="df3ff-115">This can occur even if the object and client applications were written in different programming languages.</span></span> <span data-ttu-id="df3ff-116">COM/DCOM 執行時間環境也可以使用類型程式庫，為類型程式庫中所述的介面提供自動跨單元、跨進程和跨電腦封送處理。</span><span class="sxs-lookup"><span data-stu-id="df3ff-116">The COM/DCOM run-time environment can also use a type library to provide automatic cross-apartment, cross-process, and cross-machine marshaling for interfaces described in type libraries.</span></span>

## <a name="characteristics-of-an-interface"></a><span data-ttu-id="df3ff-117">介面的特性</span><span class="sxs-lookup"><span data-stu-id="df3ff-117">Characteristics of an Interface</span></span>

<span data-ttu-id="df3ff-118">您可以在介面定義中定義介面的特性， (IDL) 檔和選擇性的應用程式佈建檔 (ACF) ：</span><span class="sxs-lookup"><span data-stu-id="df3ff-118">You define the characteristics of an interface in an interface definition (IDL) file and an optional application configuration file (ACF):</span></span>

-   <span data-ttu-id="df3ff-119">IDL 檔案指定應用程式介面在網路上的特性，也就是在用戶端與伺服器之間，或在 COM 物件之間傳輸資料的方式。</span><span class="sxs-lookup"><span data-stu-id="df3ff-119">The IDL file specifies the characteristics of the application's interfaces on the wire — that is, how data is to be transmitted between client and server, or between COM objects.</span></span>
-   <span data-ttu-id="df3ff-120">ACF 檔案會指定僅與本機作業環境相關的介面特性，例如系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="df3ff-120">The ACF file specifies interface characteristics, such as binding handles, that pertain only to the local operating environment.</span></span> <span data-ttu-id="df3ff-121">ACF 檔案也可以指定如何在獨立于電腦的表單中封送處理和傳輸複雜的資料結構。</span><span class="sxs-lookup"><span data-stu-id="df3ff-121">The ACF file can also specify how to marshal and transmit a complex data structure in a machine-independent form.</span></span>

<span data-ttu-id="df3ff-122">如需 IDL 和 ACF 檔案的詳細資訊，請參閱 [idl 和 ACF](/windows/desktop/Rpc/the-idl-and-acf-files)檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-122">For more information on IDL and ACF files, see [The IDL and ACF Files](/windows/desktop/Rpc/the-idl-and-acf-files).</span></span>

<span data-ttu-id="df3ff-123">IDL 和 ACF 檔案是以 Microsoft 介面定義語言撰寫的腳本 (MIDL) ，也就是憑證-DCE 介面定義語言 (IDL) 的 Microsoft 執行和延伸模組。</span><span class="sxs-lookup"><span data-stu-id="df3ff-123">The IDL and ACF files are scripts written in Microsoft Interface Definition Language (MIDL), which is the Microsoft implementation and extension of the OSF-DCE interface definition language (IDL).</span></span> <span data-ttu-id="df3ff-124">IDL 語言的 Microsoft 擴充功能可讓您建立 COM 介面和類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="df3ff-124">The Microsoft extensions to the IDL language enable you to create COM interfaces and type libraries.</span></span> <span data-ttu-id="df3ff-125">編譯器 Midl.exe 會使用這些腳本來產生 C 語言的存根和標頭檔，以及類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-125">The compiler, Midl.exe, uses these scripts to generate C-language stubs and header files as well as type library files.</span></span>

## <a name="the-midl-compiler"></a><span data-ttu-id="df3ff-126">MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="df3ff-126">The MIDL Compiler</span></span>

<span data-ttu-id="df3ff-127">根據 IDL 檔案的內容而定，MIDL 編譯器將會產生下列任何檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-127">Depending on the contents of your IDL file, the MIDL compiler will generate any of the following files.</span></span>

<span data-ttu-id="df3ff-128">C 語言 proxy/stub 檔案、介面識別碼檔案、DLL 資料檔案，以及自訂 COM 介面的相關標頭檔。</span><span class="sxs-lookup"><span data-stu-id="df3ff-128">A C-language proxy/stub file, an interface identifier file, a DLL data file, and a related header file for a custom COM interface.</span></span> <span data-ttu-id="df3ff-129">當 MIDL 編譯器遇到介面屬性清單中的物件屬性時，會產生這些檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-129">The MIDL compiler generates these files when it encounters the object attribute in an interface attribute list.</span></span> <span data-ttu-id="df3ff-130">如需這些檔案的詳細資訊，請參閱 [針對 COM 介面產生的](files-generated-for-a-com-interface.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-130">For more detailed information on these files, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md).</span></span>

<span data-ttu-id="df3ff-131">已編譯的類型程式庫 ( .tlb) 檔案和相關標頭檔。</span><span class="sxs-lookup"><span data-stu-id="df3ff-131">A compiled type library (.tlb) file and related header file.</span></span> <span data-ttu-id="df3ff-132">當 MIDL 遇到 IDL 檔案中的連結 [**庫**](library.md) 語句時，會產生這些檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-132">MIDL generates these files when it encounters a [**library**](library.md) statement in the IDL file.</span></span> <span data-ttu-id="df3ff-133">如需型別程式庫的一般資訊，請參閱《 Automation 程式設計人員參考》中的 [類型程式庫內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)。</span><span class="sxs-lookup"><span data-stu-id="df3ff-133">For general information about type libraries, see [Contents of a Type Library](/previous-versions/windows/desktop/automat/contents-of-a-type-library), in the Automation Programmer's Reference.</span></span>

<span data-ttu-id="df3ff-134">C/c + +-語言用戶端和伺服器 stub 檔案，以及 RPC 介面的相關標頭檔。</span><span class="sxs-lookup"><span data-stu-id="df3ff-134">C/C++-language client and server stub files and related header file for an RPC interface.</span></span> <span data-ttu-id="df3ff-135">當 IDL 檔案中沒有 [**物件**](object.md) 屬性的介面時，就會產生這些檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-135">These files are generated when there are interfaces in the IDL file that do not have the [**object**](object.md) attribute.</span></span> <span data-ttu-id="df3ff-136">如需存根和標頭檔的總覽，請參閱 [一般組建](/windows/desktop/Rpc/general-build-procedure)程式。</span><span class="sxs-lookup"><span data-stu-id="df3ff-136">For an overview of the stub and header files, see [General Build Procedure](/windows/desktop/Rpc/general-build-procedure).</span></span> <span data-ttu-id="df3ff-137">如需詳細資訊，請參閱 [針對 RPC 介面產生的](files-generated-for-an-rpc-interface.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="df3ff-137">For more detailed information, see [Files Generated for an RPC Interface](files-generated-for-an-rpc-interface.md).</span></span>

 

 