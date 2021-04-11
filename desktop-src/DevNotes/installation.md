---
description: 安裝
ms.assetid: 02A7866F-0F72-4437-A882-EEE9C2E28EC7
title: '安裝 (開發人員注意事項) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ddb476b6688bbbbef27eab571e3219071656a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847455"
---
# <a name="installation-developer-notes"></a><span data-ttu-id="1b3c7-103">安裝 (開發人員注意事項) </span><span class="sxs-lookup"><span data-stu-id="1b3c7-103">Installation (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b3c7-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="1b3c7-104">In this section</span></span>

-   [<span data-ttu-id="1b3c7-105">**CoInstall**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-105">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
-   [<span data-ttu-id="1b3c7-106">**IcfgInstallInetComponents**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-106">**IcfgInstallInetComponents**</span></span>](icfginstallinetcomponents.md)
-   [<span data-ttu-id="1b3c7-107">**IcfgNeedInetComponents**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-107">**IcfgNeedInetComponents**</span></span>](icfgneedinetcomponents.md)
-   [<span data-ttu-id="1b3c7-108">**InstallCatalog**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-108">**InstallCatalog**</span></span>](installcatalog.md)
-   [<span data-ttu-id="1b3c7-109">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-109">**InstallComponentW**</span></span>](installcomponentw.md)
-   [<span data-ttu-id="1b3c7-110">**InstallPerfDll**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-110">**InstallPerfDll**</span></span>](/windows/desktop/api/LoadPerf/nf-loadperf-installperfdlla)
-   [<span data-ttu-id="1b3c7-111">**LoadLibraryShim**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-111">**LoadLibraryShim**</span></span>](loadlibraryshim.md)
-   [<span data-ttu-id="1b3c7-112">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-112">**OcInitialize**</span></span>](ocinitialize.md)
-   [<span data-ttu-id="1b3c7-113">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-113">**OcTerminate**</span></span>](octerminate.md)
-   [<span data-ttu-id="1b3c7-114">**pSetupGetFileTitle**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-114">**pSetupGetFileTitle**</span></span>](psetupgetfiletitle.md)
-   [<span data-ttu-id="1b3c7-115">**pSetupGetGlobalFlags**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-115">**pSetupGetGlobalFlags**</span></span>](psetupgetglobalflags.md)
-   [<span data-ttu-id="1b3c7-116">**pSetupInstallCatalog**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-116">**pSetupInstallCatalog**</span></span>](psetupinstallcatalog.md)
-   [<span data-ttu-id="1b3c7-117">**pSetupIsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-117">**pSetupIsUserAdmin**</span></span>](psetupisuseradmin.md)
-   [<span data-ttu-id="1b3c7-118">**pSetupSetGlobalFlags**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-118">**pSetupSetGlobalFlags**</span></span>](psetupsetglobalflags.md)
-   [<span data-ttu-id="1b3c7-119">**pSetupStringTableDestroy**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-119">**pSetupStringTableDestroy**</span></span>](psetupstringtabledestroy.md)
-   [<span data-ttu-id="1b3c7-120">**pSetupStringTableAddStringEx**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-120">**pSetupStringTableAddStringEx**</span></span>](psetupstringtableaddstringex.md)
-   [<span data-ttu-id="1b3c7-121">**pSetupStringTableInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-121">**pSetupStringTableInitializeEx**</span></span>](psetupstringtableinitializeex.md)
-   [<span data-ttu-id="1b3c7-122">**pSetupStringTableInitialize**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-122">**pSetupStringTableInitialize**</span></span>](psetupstringtableinitialize.md)
-   [<span data-ttu-id="1b3c7-123">**pSetupVerifyCatalogFile**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-123">**pSetupVerifyCatalogFile**</span></span>](psetupverifycatalogfile.md)
-   [<span data-ttu-id="1b3c7-124">**重載 \_ config**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-124">**reload\_config**</span></span>](reload-config.md)
-   [<span data-ttu-id="1b3c7-125">**SxsLookupClrGuid**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-125">**SxsLookupClrGuid**</span></span>](sxslookupclrguid.md)
-   [<span data-ttu-id="1b3c7-126">**UninstallComponent**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-126">**UninstallComponent**</span></span>](uninstallcomponent.md)
-   [<span data-ttu-id="1b3c7-127">**VerifyCatalogFile**</span><span class="sxs-lookup"><span data-stu-id="1b3c7-127">**VerifyCatalogFile**</span></span>](verifycatalogfile.md)

 

 
