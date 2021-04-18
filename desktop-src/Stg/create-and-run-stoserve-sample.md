---
title: 建立並執行 StoServe 範例
description: 您必須先編譯用戶端範例和其他相關的範例，才能執行用戶端。
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965785"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="9c738-103">建立並執行 StoServe 範例</span><span class="sxs-lookup"><span data-stu-id="9c738-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="9c738-104">您必須先編譯用戶端範例和其他相關的範例，才能執行用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c738-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="9c738-105">如需建立範例的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="9c738-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="9c738-106">如果您已經建立適當的範例，STOCLIEN.EXE 是執行 **StoServe** 範例的用戶端可執行檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="9c738-107">程式碼導覽</span><span class="sxs-lookup"><span data-stu-id="9c738-107">Code Tour</span></span>

<span data-ttu-id="9c738-108">下表列出與 **StoServe** 範例相關的檔案。</span><span class="sxs-lookup"><span data-stu-id="9c738-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="9c738-109">檔案</span><span class="sxs-lookup"><span data-stu-id="9c738-109">Files</span></span>        | <span data-ttu-id="9c738-110">Description</span><span class="sxs-lookup"><span data-stu-id="9c738-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c738-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="9c738-111">STOSERVE.TXT</span></span> | <span data-ttu-id="9c738-112">簡短範例描述</span><span class="sxs-lookup"><span data-stu-id="9c738-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="9c738-113">生成</span><span class="sxs-lookup"><span data-stu-id="9c738-113">MAKEFILE</span></span>     | <span data-ttu-id="9c738-114">用來建立本課程 STOSERVE.DLL 程式碼範例的一般 makefile。</span><span class="sxs-lookup"><span data-stu-id="9c738-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="9c738-115">STOSERVE.H</span><span class="sxs-lookup"><span data-stu-id="9c738-115">STOSERVE.H</span></span>   | <span data-ttu-id="9c738-116">在 STOSERVE.DLL 中宣告為已匯入或定義為已匯出服務函數的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="9c738-117">STOSERVE.Cpp</span><span class="sxs-lookup"><span data-stu-id="9c738-117">STOSERVE.CPP</span></span> | <span data-ttu-id="9c738-118">STOSERVE.DLL 的主要執行檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="9c738-119">具有 DllMain 和 COM 伺服器函數 (例如，DllGetClassObject) 。</span><span class="sxs-lookup"><span data-stu-id="9c738-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="9c738-120">STOSERVE.Def</span><span class="sxs-lookup"><span data-stu-id="9c738-120">STOSERVE.DEF</span></span> | <span data-ttu-id="9c738-121">模組定義檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-121">The module definition file.</span></span> <span data-ttu-id="9c738-122">匯出伺服器架函數。</span><span class="sxs-lookup"><span data-stu-id="9c738-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="9c738-123">STOSERVE.鋼筋混凝土</span><span class="sxs-lookup"><span data-stu-id="9c738-123">STOSERVE.RC</span></span>  | <span data-ttu-id="9c738-124">可執行檔的 DLL 資源定義檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="9c738-125">STOSERVE..ICO</span><span class="sxs-lookup"><span data-stu-id="9c738-125">STOSERVE.ICO</span></span> | <span data-ttu-id="9c738-126">可執行檔的圖示資源。</span><span class="sxs-lookup"><span data-stu-id="9c738-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="9c738-127">伺服器。H</span><span class="sxs-lookup"><span data-stu-id="9c738-127">SERVER.H</span></span>     | <span data-ttu-id="9c738-128">伺服器控制項 c + + 物件的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="9c738-129">伺服器。Cpp</span><span class="sxs-lookup"><span data-stu-id="9c738-129">SERVER.CPP</span></span>   | <span data-ttu-id="9c738-130">伺服器控制項 c + + 物件的執行檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="9c738-131">廠。H</span><span class="sxs-lookup"><span data-stu-id="9c738-131">FACTORY.H</span></span>    | <span data-ttu-id="9c738-132">伺服器的 class factory COM 物件的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="9c738-133">廠。Cpp</span><span class="sxs-lookup"><span data-stu-id="9c738-133">FACTORY.CPP</span></span>  | <span data-ttu-id="9c738-134">伺服器的 class factory 的執行檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="9c738-135">連接。H</span><span class="sxs-lookup"><span data-stu-id="9c738-135">CONNECT.H</span></span>    | <span data-ttu-id="9c738-136">連接點列舉值、連接點和連接列舉值類別的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="9c738-137">連接。Cpp</span><span class="sxs-lookup"><span data-stu-id="9c738-137">CONNECT.CPP</span></span>  | <span data-ttu-id="9c738-138">連接點列舉值、連接點和連接列舉值物件的執行檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="9c738-139">紙。H</span><span class="sxs-lookup"><span data-stu-id="9c738-139">PAPER.H</span></span>      | <span data-ttu-id="9c738-140">COPaper COM 物件類別的 include 檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="9c738-141">紙。Cpp</span><span class="sxs-lookup"><span data-stu-id="9c738-141">PAPER.CPP</span></span>    | <span data-ttu-id="9c738-142">COPaper COM 物件類別和連接點的實檔案。</span><span class="sxs-lookup"><span data-stu-id="9c738-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="9c738-143">STOSERVE.Dsp</span><span class="sxs-lookup"><span data-stu-id="9c738-143">STOSERVE.DSP</span></span> | <span data-ttu-id="9c738-144">Microsoft Visual Studio 專案檔。</span><span class="sxs-lookup"><span data-stu-id="9c738-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="9c738-145">本程式碼教學課程中涵蓋的主要主題如下：</span><span class="sxs-lookup"><span data-stu-id="9c738-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="9c738-146">[**IPaper**](ipaper-methods.md)介面方法。</span><span class="sxs-lookup"><span data-stu-id="9c738-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="9c738-147">COPaper 使用 [**IPaperSink**](ipapersink-methods.md) 介面來進行用戶端通知。</span><span class="sxs-lookup"><span data-stu-id="9c738-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="9c738-148">StoServe 中的 [**結構**](structures---stoserve.md)。</span><span class="sxs-lookup"><span data-stu-id="9c738-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="9c738-149">[Unicode 考慮事項](unicode-considerations.md)。</span><span class="sxs-lookup"><span data-stu-id="9c738-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




