---
description: COM + 提供的系統管理物件模型會公開 [元件服務] 系統管理工具的所有功能，它本身是以系統管理物件為基礎所撰寫的圖形前端。
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: 自動化 COM + 管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111048"
---
# <a name="automating-com-administration"></a><span data-ttu-id="866df-103">自動化 COM + 管理</span><span class="sxs-lookup"><span data-stu-id="866df-103">Automating COM+ Administration</span></span>

<span data-ttu-id="866df-104">COM + 提供的系統管理物件模型會公開 [元件服務] 系統管理工具的所有功能，它本身是以系統管理物件為基礎所撰寫的圖形前端。</span><span class="sxs-lookup"><span data-stu-id="866df-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="866df-105">您可以使用元件服務管理 (COMAdmin) 程式庫所提供的這些物件，將 COM + 應用程式和服務管理中的所有工作自動化。</span><span class="sxs-lookup"><span data-stu-id="866df-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="866df-106">COMAdmin 物件可讓您讀取和寫入儲存在 COM + 目錄中的資訊，這是保存所有 COM + 設定資料的基礎資料存放區。</span><span class="sxs-lookup"><span data-stu-id="866df-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="866df-107">您可以使用這些物件來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="866df-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="866df-108">建立和設定 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="866df-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="866df-109">安裝和匯出現有的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="866df-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="866df-110">管理已安裝的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="866df-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="866df-111">管理和設定服務。</span><span class="sxs-lookup"><span data-stu-id="866df-111">Manage and configure services.</span></span>
-   <span data-ttu-id="866df-112">在不同的電腦上遠端系統管理元件服務。</span><span class="sxs-lookup"><span data-stu-id="866df-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="866df-113">您可以使用可編寫腳本的 COMAdmin 物件搭配任何自動化相容語言，例如 Microsoft Visual Basic 和 Visual Basic 腳本。</span><span class="sxs-lookup"><span data-stu-id="866df-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="866df-114">您可以開發輕量腳本或一般用途的管理工具。</span><span class="sxs-lookup"><span data-stu-id="866df-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="866df-115">例如，您可以：</span><span class="sxs-lookup"><span data-stu-id="866df-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="866df-116">撰寫腳本來執行例行的系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="866df-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="866df-117">撰寫腳本，以在開發 COM + 應用程式的過程中自動執行程式。</span><span class="sxs-lookup"><span data-stu-id="866df-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="866df-118">開發用來管理和監視元件服務的一般用途工具。</span><span class="sxs-lookup"><span data-stu-id="866df-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="866df-119">開發安裝程式可執行檔，以安裝及部署您的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="866df-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="866df-120">COMAdmin 程式庫提供與 MTS 2.0 管理程式庫的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="866df-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="866df-121">雖然有一些例外狀況，但大部分現有的 MTS 2.0 管理程式碼仍可運作。</span><span class="sxs-lookup"><span data-stu-id="866df-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="866df-122"> (參閱 [MTS 管理程式庫](mts-administration-library.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="866df-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="866df-123">若要有效率地自動化管理，您應該熟悉使用 [元件服務] 系統管理工具執行的系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="866df-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="866df-124">如需 COMAdmin 物件和對應介面的完整說明，請參閱下列類別和介面的 COM + 參考檔：</span><span class="sxs-lookup"><span data-stu-id="866df-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="866df-125">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="866df-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="866df-126">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="866df-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="866df-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="866df-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="866df-128">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="866df-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="866df-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="866df-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="866df-130">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="866df-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="866df-131">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="866df-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="866df-132">本節中的下列主題提供使用 COMAdmin 物件自動化管理的總覽：</span><span class="sxs-lookup"><span data-stu-id="866df-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="866df-133">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="866df-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="866df-134">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="866df-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="866df-135">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="866df-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="866df-136">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="866df-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="866df-137">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="866df-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="866df-138">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="866df-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 



