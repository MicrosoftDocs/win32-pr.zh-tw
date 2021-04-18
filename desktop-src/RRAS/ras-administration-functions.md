---
title: RAS 管理功能
description: 本檔說明用來開發軟體來管理 RAS 撥號連線的 RRAS 函數。
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301900"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="65c4f-103">RAS 管理功能</span><span class="sxs-lookup"><span data-stu-id="65c4f-103">RAS Administration Functions</span></span>

<span data-ttu-id="65c4f-104">本檔說明用來開發軟體來管理 RAS 撥號連線的 RRAS 函數。</span><span class="sxs-lookup"><span data-stu-id="65c4f-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="65c4f-105">這些功能包括：</span><span class="sxs-lookup"><span data-stu-id="65c4f-105">These functions include:</span></span>

-   [<span data-ttu-id="65c4f-106">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="65c4f-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="65c4f-107">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="65c4f-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="65c4f-108">**MprAdminConnectionEnumEx**</span><span class="sxs-lookup"><span data-stu-id="65c4f-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="65c4f-109">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="65c4f-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="65c4f-110">**MprAdminConnectionGetInfoEx**</span><span class="sxs-lookup"><span data-stu-id="65c4f-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="65c4f-111">**MprAdminConnectionRemoveQuarantine**</span><span class="sxs-lookup"><span data-stu-id="65c4f-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="65c4f-112">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="65c4f-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="65c4f-113">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="65c4f-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="65c4f-114">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="65c4f-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="65c4f-115">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="65c4f-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="65c4f-116">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="65c4f-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="65c4f-117">額外的函式可用於 RAS 管理與路由器管理。</span><span class="sxs-lookup"><span data-stu-id="65c4f-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="65c4f-118">下列功能記載于 [路由器管理功能](router-administration-functions.md) 參考中：</span><span class="sxs-lookup"><span data-stu-id="65c4f-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="65c4f-119">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="65c4f-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="65c4f-120">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="65c4f-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="65c4f-121">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="65c4f-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="65c4f-122">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="65c4f-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="65c4f-123">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="65c4f-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="65c4f-124">若要執行 RAS 管理 DLL，請使用下列主題中所述的功能：</span><span class="sxs-lookup"><span data-stu-id="65c4f-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="65c4f-125">RAS 系統管理 DLL 函式</span><span class="sxs-lookup"><span data-stu-id="65c4f-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="65c4f-126">若要管理 RAS 伺服器的使用者，請使用下列主題中所述的功能：</span><span class="sxs-lookup"><span data-stu-id="65c4f-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="65c4f-127">RAS 使用者管理功能</span><span class="sxs-lookup"><span data-stu-id="65c4f-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




