---
title: 功能比較 Windows 2000 與 RRAS 可轉散發套件
description: RAS API 是以 Windows 2000 和更新版本作業系統的一項功能來散發，並可作為 Windows NT 4.0 Service Pack 3 (SP3) 及更早版本的可轉散發套件。
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966004"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="0026e-103">函數比較： Windows 2000 與 RRAS 可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0026e-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="0026e-104">RAS API 是以 Windows 2000 和更新版本作業系統的一項功能來散發，並可作為 Windows NT 4.0 Service Pack 3 (SP3) 及更早版本的可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="0026e-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="0026e-105">RAS 在這兩種形式中都提供相同的功能，但每個 RAS API 版本中的參考元素都會使用不同的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="0026e-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="0026e-106">Windows NT 4.0 SP3 和較早版本的 RAS 函式通常會以 "RasAdmin" 前置詞作為開頭。</span><span class="sxs-lookup"><span data-stu-id="0026e-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="0026e-107">路由及遠端存取服務 (RRAS 的類似功能) 以 "MprAdmin" 前置詞為開頭。</span><span class="sxs-lookup"><span data-stu-id="0026e-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="0026e-108">例如，RAS 提供稱為 [**RasAdminPortGetInfo**](rasadminportgetinfo.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="0026e-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="0026e-109">RRAS 中類似的函式稱為 [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)。</span><span class="sxs-lookup"><span data-stu-id="0026e-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="0026e-110">就像範例一樣，RAS 提供回呼函式 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)。</span><span class="sxs-lookup"><span data-stu-id="0026e-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="0026e-111">RRAS 提供類似的回呼函數，稱為 [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)。</span><span class="sxs-lookup"><span data-stu-id="0026e-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="0026e-112">這項規則的例外狀況是 [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)，在 rras 下是 [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)，而 [**RasAdminFreeBuffer**](rasadminfreebuffer.md)則是 [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)。</span><span class="sxs-lookup"><span data-stu-id="0026e-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="0026e-113">下表列出 Windows NT 4.0 SP3 RAS 函式和對應的 RRAS 函數。</span><span class="sxs-lookup"><span data-stu-id="0026e-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="0026e-114">Windows NT 4.0 RAS</span><span class="sxs-lookup"><span data-stu-id="0026e-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="0026e-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="0026e-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0026e-116">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="0026e-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="0026e-117">**MprAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="0026e-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="0026e-118">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="0026e-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="0026e-119">**MprAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="0026e-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="0026e-120">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="0026e-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="0026e-121">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="0026e-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="0026e-122">**RasAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="0026e-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="0026e-123">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="0026e-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="0026e-124">**RasAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="0026e-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="0026e-125">**MprAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="0026e-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="0026e-126">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="0026e-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="0026e-127">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="0026e-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="0026e-128">**RasAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0026e-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="0026e-129">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0026e-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="0026e-130">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="0026e-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="0026e-131">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="0026e-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="0026e-132">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="0026e-133">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="0026e-134">**RasAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="0026e-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="0026e-135">**MprAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="0026e-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="0026e-136">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="0026e-137">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="0026e-138">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="0026e-139">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="0026e-140">雖然 RRAS 函數類似于其 Windows NT 4.0 與 SP3 以及舊版的 RAS 對應功能，但 RRAS 函數通常會採用一組不同的參數。</span><span class="sxs-lookup"><span data-stu-id="0026e-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="0026e-141">如需該函式參數清單的完整資訊，請參閱特定函式的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="0026e-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="0026e-142">適用于 Windows NT 4.0 SP3 及更早版本的 RRAS 可轉散發套件會新增下列沒有 RAS 對應專案的函式：</span><span class="sxs-lookup"><span data-stu-id="0026e-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="0026e-143">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="0026e-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="0026e-144">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="0026e-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="0026e-145">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="0026e-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="0026e-146">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0026e-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="0026e-147">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="0026e-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="0026e-148">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="0026e-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="0026e-149">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="0026e-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="0026e-150">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="0026e-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="0026e-151">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="0026e-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="0026e-152">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0026e-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="0026e-153">除了上述的函式，Windows 2000 和更新版本的作業系統也會新增下列功能：</span><span class="sxs-lookup"><span data-stu-id="0026e-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="0026e-154">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="0026e-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="0026e-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="0026e-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="0026e-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="0026e-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




