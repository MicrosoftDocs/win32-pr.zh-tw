---
title: MIDL 編譯
description: MIDL 編譯
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463757"
---
# <a name="midl-compilation"></a><span data-ttu-id="31e39-103">MIDL 編譯</span><span class="sxs-lookup"><span data-stu-id="31e39-103">MIDL Compilation</span></span>

<span data-ttu-id="31e39-104">給定 IDL 檔案（如 [Example2](anatomy-of-an-idl-file.md)），它會定義一或多個 COM 介面和類型程式庫，MIDL 編譯器 (Midl.exe) 會產生下表中所述的檔案做為預設輸出。</span><span class="sxs-lookup"><span data-stu-id="31e39-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="31e39-105">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="31e39-105">Filename</span></span>                 | <span data-ttu-id="31e39-106">描述</span><span class="sxs-lookup"><span data-stu-id="31e39-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e39-107">Example2。h</span><span class="sxs-lookup"><span data-stu-id="31e39-107">Example2.h</span></span><br/>    | <span data-ttu-id="31e39-108">標頭檔案，其中包含 IDL 檔案中定義之所有介面的類型定義和函式宣告，以及存根所呼叫之常式的向前宣告。</span><span class="sxs-lookup"><span data-stu-id="31e39-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="31e39-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="31e39-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="31e39-110">Proxy/stub 檔案，其中包含用戶端和伺服器的代理進入點。</span><span class="sxs-lookup"><span data-stu-id="31e39-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="31e39-111">Example2 \_ c。</span><span class="sxs-lookup"><span data-stu-id="31e39-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="31e39-112">介面識別碼檔案，這個檔案會定義 IDL 檔案中指定之每個介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="31e39-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="31e39-113">Example2 .tlb</span><span class="sxs-lookup"><span data-stu-id="31e39-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="31e39-114">複合檔案檔案，其中包含類型和物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31e39-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="31e39-115">Dlldata.c。c</span><span class="sxs-lookup"><span data-stu-id="31e39-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="31e39-116">包含建立 proxy/stub DLL 所需的資料。</span><span class="sxs-lookup"><span data-stu-id="31e39-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="31e39-117">當用戶端應用程式和物件服務器使用此檔案時，您可以使用標頭檔和所有 .c 檔案來建立可支援介面的 [PROXY DLL](building-and-registering-a-proxy-dll.md) 。</span><span class="sxs-lookup"><span data-stu-id="31e39-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="31e39-118">\_當您為使用介面的用戶端應用程式建立可執行檔時，您可以使用 (Example2 的介面標頭檔) 和介面識別碼 (Example2 的) 檔。</span><span class="sxs-lookup"><span data-stu-id="31e39-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="31e39-119">您可以選擇在 EXE 或 DLL 中以資源的形式包含類型程式庫檔案，也可以將它當作個別檔案來傳送。</span><span class="sxs-lookup"><span data-stu-id="31e39-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31e39-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="31e39-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31e39-121">針對 COM 介面產生的檔案</span><span class="sxs-lookup"><span data-stu-id="31e39-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="31e39-122">MIDL 編譯器選項</span><span class="sxs-lookup"><span data-stu-id="31e39-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

