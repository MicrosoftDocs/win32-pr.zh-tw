---
title: '資源功能 (功能表和其他資源) '
description: .
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb29a106483a26dbf249a0046ca0ab53105d975
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024464"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="37115-103">資源功能 (功能表和其他資源) </span><span class="sxs-lookup"><span data-stu-id="37115-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37115-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="37115-104">In This Section</span></span>

-   [<span data-ttu-id="37115-105">**BeginUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="37115-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="37115-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="37115-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="37115-107">**EndUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="37115-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="37115-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37115-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="37115-109">*EnumResNameProc*</span><span class="sxs-lookup"><span data-stu-id="37115-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="37115-110">**EnumResourceLanguages**</span><span class="sxs-lookup"><span data-stu-id="37115-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="37115-111">**EnumResourceLanguagesEx**</span><span class="sxs-lookup"><span data-stu-id="37115-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="37115-112">**EnumResourceNames**</span><span class="sxs-lookup"><span data-stu-id="37115-112">**EnumResourceNames**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcenamesa)
-   [<span data-ttu-id="37115-113">**EnumResourceNamesEx**</span><span class="sxs-lookup"><span data-stu-id="37115-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="37115-114">**EnumResourceTypes**</span><span class="sxs-lookup"><span data-stu-id="37115-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="37115-115">**EnumResourceTypesEx**</span><span class="sxs-lookup"><span data-stu-id="37115-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="37115-116">*EnumResTypeProc*</span><span class="sxs-lookup"><span data-stu-id="37115-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="37115-117">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="37115-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="37115-118">**FindResourceEx**</span><span class="sxs-lookup"><span data-stu-id="37115-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="37115-119">**FreeResource**</span><span class="sxs-lookup"><span data-stu-id="37115-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="37115-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="37115-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="37115-121">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="37115-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="37115-122">**LockResource**</span><span class="sxs-lookup"><span data-stu-id="37115-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="37115-123">**SizeofResource**</span><span class="sxs-lookup"><span data-stu-id="37115-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="37115-124">**UpdateResource**</span><span class="sxs-lookup"><span data-stu-id="37115-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
