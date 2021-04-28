---
title: '資源功能 (功能表和其他資源) '
description: '資源功能 (功能表和其他資源) '
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e550bd42afcb98d2a1d7b1117c6c93d19529c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117526"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="9fac6-103">資源功能 (功能表和其他資源) </span><span class="sxs-lookup"><span data-stu-id="9fac6-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fac6-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="9fac6-104">In This Section</span></span>

-   [<span data-ttu-id="9fac6-105">**BeginUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="9fac6-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="9fac6-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="9fac6-107">**EndUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="9fac6-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fac6-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="9fac6-109">*EnumResNameProc*</span><span class="sxs-lookup"><span data-stu-id="9fac6-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="9fac6-110">**EnumResourceLanguages**</span><span class="sxs-lookup"><span data-stu-id="9fac6-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="9fac6-111">**EnumResourceLanguagesEx**</span><span class="sxs-lookup"><span data-stu-id="9fac6-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="9fac6-112">**EnumResourceNames**</span><span class="sxs-lookup"><span data-stu-id="9fac6-112">**EnumResourceNames**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcenamesa)
-   [<span data-ttu-id="9fac6-113">**EnumResourceNamesEx**</span><span class="sxs-lookup"><span data-stu-id="9fac6-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="9fac6-114">**EnumResourceTypes**</span><span class="sxs-lookup"><span data-stu-id="9fac6-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="9fac6-115">**EnumResourceTypesEx**</span><span class="sxs-lookup"><span data-stu-id="9fac6-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="9fac6-116">*EnumResTypeProc*</span><span class="sxs-lookup"><span data-stu-id="9fac6-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="9fac6-117">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="9fac6-118">**FindResourceEx**</span><span class="sxs-lookup"><span data-stu-id="9fac6-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="9fac6-119">**FreeResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="9fac6-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="9fac6-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="9fac6-121">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="9fac6-122">**LockResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="9fac6-123">**SizeofResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="9fac6-124">**UpdateResource**</span><span class="sxs-lookup"><span data-stu-id="9fac6-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
