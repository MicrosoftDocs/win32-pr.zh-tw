---
title: RAS 系統管理 DLL 函式
description: RAS 系統管理 DLL 必須執行並匯出下列所有功能
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a02c8dc9212f3cfd173c9a236f81fcf766658424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682807"
---
# <a name="ras-administration-dll-functions"></a><span data-ttu-id="54efd-103">RAS 系統管理 DLL 函式</span><span class="sxs-lookup"><span data-stu-id="54efd-103">RAS administration DLL functions</span></span>

<span data-ttu-id="54efd-104">RAS 系統管理 DLL 必須執行並匯出下列所有功能：</span><span class="sxs-lookup"><span data-stu-id="54efd-104">A RAS administration DLL must implement and export all of the following functions:</span></span>

-   [<span data-ttu-id="54efd-105">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="54efd-105">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   <span data-ttu-id="54efd-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication)或 [ **MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span><span class="sxs-lookup"><span data-stu-id="54efd-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) or [**MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span></span>
-   <span data-ttu-id="54efd-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)或 [ **MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span><span class="sxs-lookup"><span data-stu-id="54efd-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) or [**MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span></span>
-   [<span data-ttu-id="54efd-108">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="54efd-108">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [<span data-ttu-id="54efd-109">**MprAdminTerminateDll**</span><span class="sxs-lookup"><span data-stu-id="54efd-109">**MprAdminTerminateDll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

<span data-ttu-id="54efd-110">**Windows 2000/NT：** RAS 管理 DLL 也必須執行和匯出下列成對的函式： [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) 和 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="54efd-110">**Windows 2000/NT:** The RAS administration DLL must also implement and export the following pair of functions: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>

<span data-ttu-id="54efd-111">此外，「RAS 管理」 DLL 必須執行並匯出下列其中一組函數：</span><span class="sxs-lookup"><span data-stu-id="54efd-111">In addition, the RAS administration DLL must implement and export one of the following pairs of functions:</span></span>

-   <span data-ttu-id="54efd-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)和 [ **MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span><span class="sxs-lookup"><span data-stu-id="54efd-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) and [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span></span>
-   <span data-ttu-id="54efd-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)和 [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span><span class="sxs-lookup"><span data-stu-id="54efd-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) and [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span></span>
-   <span data-ttu-id="54efd-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3)和 [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span><span class="sxs-lookup"><span data-stu-id="54efd-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) and [**MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span></span>
-   <span data-ttu-id="54efd-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex)和 [ **MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span><span class="sxs-lookup"><span data-stu-id="54efd-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) and [**MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span></span>

<span data-ttu-id="54efd-116">如果未執行其中一個必要的函式，則遠端存取服務無法啟動。</span><span class="sxs-lookup"><span data-stu-id="54efd-116">If one of the required functions is not implemented, the remote access service fails to start.</span></span>

<span data-ttu-id="54efd-117">若要執行下列成對的函式，則不需要管理 DLL：</span><span class="sxs-lookup"><span data-stu-id="54efd-117">An administration DLL is not required to implement the following pairs of functions:</span></span>

-   <span data-ttu-id="54efd-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)和 [ **MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="54efd-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>
-   <span data-ttu-id="54efd-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser)和 [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span><span class="sxs-lookup"><span data-stu-id="54efd-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) and [*MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span></span>

<span data-ttu-id="54efd-120">但是，如果 DLL 在上面所列的組中執行一個函式，則它也必須在配對中執行另一個函數。</span><span class="sxs-lookup"><span data-stu-id="54efd-120">However, if the DLL implements one function in a pair listed above, it must implement the other function in the pair as well.</span></span>

<span data-ttu-id="54efd-121">如需有關 RAS 管理 Dll 的詳細資訊，請參閱「 [Ras 管理 dll](ras-administration-dll.md)」的「總覽」主題。</span><span class="sxs-lookup"><span data-stu-id="54efd-121">For more information on RAS Administration DLLs, see the overview topic, [RAS Administration DLL](ras-administration-dll.md).</span></span>

 

 