---
title: COM 程式庫
description: COM 程式庫
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2020
ms.locfileid: "103932991"
---
# <a name="the-com-library"></a><span data-ttu-id="f9429-103">COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="f9429-103">The COM Library</span></span>

<span data-ttu-id="f9429-104">任何使用 COM 的進程都必須初始化和解除初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="f9429-104">Any process that uses COM must both initialize and uninitialize the COM library.</span></span> <span data-ttu-id="f9429-105">除了做為規格之外，COM 也會在此程式庫中實行一些重要的服務。</span><span class="sxs-lookup"><span data-stu-id="f9429-105">In addition to being a specification, COM also implements some important services in this library.</span></span> <span data-ttu-id="f9429-106">以一組 Dll 和 Exe 的形式提供 (主要是在 Microsoft Windows 中 Ole32.dll 和 Rpcss.exe) ，COM 程式庫包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="f9429-106">Provided as a set of DLLs and EXEs (primarily Ole32.dll and Rpcss.exe) in Microsoft Windows, the COM library includes the following:</span></span>

-   <span data-ttu-id="f9429-107">許多基本功能，可協助建立 COM 應用程式（用戶端和伺服器）。</span><span class="sxs-lookup"><span data-stu-id="f9429-107">A small number of fundamental functions that facilitate the creation of COM applications, both client and server.</span></span> <span data-ttu-id="f9429-108">針對用戶端，COM 會提供基本功能來建立物件。</span><span class="sxs-lookup"><span data-stu-id="f9429-108">For clients, COM supplies basic functions for creating objects.</span></span> <span data-ttu-id="f9429-109">針對伺服器，COM 會提供公開其物件的方法。</span><span class="sxs-lookup"><span data-stu-id="f9429-109">For servers, COM supplies the means of exposing their objects.</span></span>

-   <span data-ttu-id="f9429-110">由 COM 從唯一類別識別碼 (CLSID) 的實作為定位器服務，該服務會在伺服器上執行該類別以及該伺服器所在位置。</span><span class="sxs-lookup"><span data-stu-id="f9429-110">Implementation-locator services through which COM determines, from a unique class identifier (CLSID), which server implements that class and where that server is located.</span></span> <span data-ttu-id="f9429-111">這項服務包括在物件類別的身分識別與執行封裝之間的間接取值層級（通常是系統登錄）之間的支援，以便用戶端與封裝無關（未來可能會變更）。</span><span class="sxs-lookup"><span data-stu-id="f9429-111">This service includes support for a level of indirection, usually a system registry, between the identity of an object class and the packaging of the implementation so that clients are independent of the packaging, which can change in the future.</span></span>

-   <span data-ttu-id="f9429-112">當物件在本機或遠端伺服器中執行時，透明的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9429-112">Transparent remote procedure calls when an object is running in a local or remote server.</span></span>

-   <span data-ttu-id="f9429-113">一種標準機制，可讓應用程式控制在其進程內配置記憶體的方式，特別是需要在合作物件之間傳遞的記憶體，才能正確釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="f9429-113">A standard mechanism to allow an application to control how memory is allocated within its process, particularly memory that needs to be passed between cooperating objects so that it can be freed properly.</span></span>

<span data-ttu-id="f9429-114">若要使用基本 COM 服務，在用戶端和跨進程伺服器中執行的所有 COM 執行緒都必須呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式，然後再呼叫其他任何 COM 函式，但記憶體配置呼叫除外。</span><span class="sxs-lookup"><span data-stu-id="f9429-114">To use basic COM services, all COM threads of execution in clients and out-of-process servers must call either the [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function before calling any other COM function except memory allocation calls.</span></span> <span data-ttu-id="f9429-115">**CoInitializeEx** 會取代另一個函式，加入可讓您指定執行緒執行緒模型的參數：「跨執行緒」或「無限制執行緒」。</span><span class="sxs-lookup"><span data-stu-id="f9429-115">**CoInitializeEx** replaces the other function, adding a parameter that allows you to specify the threading model of the thread: either apartment-threaded or free-threaded.</span></span> <span data-ttu-id="f9429-116">對 **CoInitialize** 的呼叫只會將執行緒模型設定為單元執行緒。</span><span class="sxs-lookup"><span data-stu-id="f9429-116">A call to **CoInitialize** simply sets the threading model to apartment-threaded.</span></span>

<span data-ttu-id="f9429-117">OLE 複合檔案應用程式會呼叫 [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) 函式，此函式會呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，也會執行複合檔案所需的部分初始化。</span><span class="sxs-lookup"><span data-stu-id="f9429-117">OLE compound document applications call the [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) function, which calls [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) and also does some initialization required for compound documents.</span></span> <span data-ttu-id="f9429-118">因此，呼叫 **OleInitialize** 的執行緒不能自由執行緒。</span><span class="sxs-lookup"><span data-stu-id="f9429-118">Therefore, threads that call **OleInitialize** cannot be free-threaded.</span></span> <span data-ttu-id="f9429-119">如需用戶端和伺服器中線程的詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。</span><span class="sxs-lookup"><span data-stu-id="f9429-119">For information on threading in clients and servers, see [Processes, Threads, and Apartments](processes--threads--and-apartments.md).</span></span>

<span data-ttu-id="f9429-120">同進程伺服器不會呼叫初始化函式，因為它們會載入至已完成的處理常式。</span><span class="sxs-lookup"><span data-stu-id="f9429-120">In-process servers do not call the initialization functions because they are being loaded into a process that has already done so.</span></span> <span data-ttu-id="f9429-121">因此，同進程伺服器必須在登錄中的 [InprocServer32](inprocserver32.md) 機碼下設定其執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="f9429-121">As a result, in-process servers must set their threading model in the registry under the [InprocServer32](inprocserver32.md) key.</span></span> <span data-ttu-id="f9429-122">如需有關同進程伺服器中線程問題的詳細資訊，請參閱同進程 [伺服器執行緒問題](in-process-server-threading-issues.md)。</span><span class="sxs-lookup"><span data-stu-id="f9429-122">For detailed information on threading issues in in-process servers, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

<span data-ttu-id="f9429-123">解除初始化程式庫也很重要。</span><span class="sxs-lookup"><span data-stu-id="f9429-123">It is also important to uninitialize the library.</span></span> <span data-ttu-id="f9429-124">對於每個 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫，都必須有對應的 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9429-124">For each call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), there must be a corresponding call to [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="f9429-125">對於 [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize)的每個呼叫，都必須有對應的 [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize)呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9429-125">For each call to [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), there must be a corresponding call to [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).</span></span>

<span data-ttu-id="f9429-126">同進程伺服器可以假設它們正在載入的進程已執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="f9429-126">In-process servers can assume that the process they are being loaded into has already performed these steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9429-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9429-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9429-128">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="f9429-128">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




