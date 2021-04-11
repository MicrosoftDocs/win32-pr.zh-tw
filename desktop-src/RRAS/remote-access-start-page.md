---
title: 遠端存取
description: 使用遠端存取服務 (RAS) 來建立用戶端應用程式。
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- 遠端存取服務 RAS
- RAS RAS
- 遠端存取服務 RAS、起始頁
- RAS RAS，請參閱遠端存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092560"
---
# <a name="remote-access"></a><span data-ttu-id="fa7c2-107">遠端存取</span><span class="sxs-lookup"><span data-stu-id="fa7c2-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="fa7c2-108">目的</span><span class="sxs-lookup"><span data-stu-id="fa7c2-108">Purpose</span></span>

<span data-ttu-id="fa7c2-109">使用遠端存取服務 (RAS) 來建立用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="fa7c2-110">這些應用程式會顯示 RAS 通用對話方塊、管理遠端存取連線和裝置，以及操作電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="fa7c2-111">RAS 也為遠端存取服務提供新一代的伺服器功能， (RAS) for Windows。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="fa7c2-112">RRAS 伺服器功能遵循，並以遠端存取服務 (RAS) 為基礎。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="fa7c2-113">適用時</span><span class="sxs-lookup"><span data-stu-id="fa7c2-113">Where applicable</span></span>

<span data-ttu-id="fa7c2-114">遠端存取服務適用于使用廣域網路 (WAN) 連結或虛擬私人網路 (VPN) 的任何計算環境。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="fa7c2-115">RAS 可以透過 WAN 連結或 VPN，將遠端用戶端電腦連線到網路伺服器。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="fa7c2-116">遠端電腦接著會在伺服器的 LAN 上運作，就好像遠端電腦直接連接到 LAN 一樣。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="fa7c2-117">RAS API 可讓程式設計人員以程式設計方式存取 RAS 的功能。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fa7c2-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="fa7c2-118">Developer audience</span></span>

<span data-ttu-id="fa7c2-119">RAS API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="fa7c2-120">Microsoft Visual Basic 程式設計人員也可能會發現 API 很有用。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="fa7c2-121">程式設計人員應該熟悉網路概念。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fa7c2-122">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="fa7c2-122">Run-time requirements</span></span>

<span data-ttu-id="fa7c2-123">只有網路伺服器上才支援 RAS API 中的部分功能，而只有網路用戶端支援其他功能。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="fa7c2-124">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="fa7c2-125">您可以藉由安裝[rras](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp)可轉散發套件，將 rras 的[增強 RAS 功能](function-comparison-windows-2000-versus-rras-redistributable.md)提供給 Windows NT Server 4.0。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="fa7c2-126">RRAS 的所有功能都整合到 Windows 2000 Server、Windows Server 2003 和 Windows Server 2008 中。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="fa7c2-127">RRAS 應用程式無法在 Windows NT 工作站4.0 或用戶端作業系統（例如 Windows 95）上執行。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="fa7c2-128">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa7c2-129">本節內容</span><span class="sxs-lookup"><span data-stu-id="fa7c2-129">In this section</span></span>



| <span data-ttu-id="fa7c2-130">主題</span><span class="sxs-lookup"><span data-stu-id="fa7c2-130">Topic</span></span>                                                                                             | <span data-ttu-id="fa7c2-131">描述</span><span class="sxs-lookup"><span data-stu-id="fa7c2-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa7c2-132">遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="fa7c2-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="fa7c2-133">遠端存取服務 (RAS) 為執行 Windows 的電腦上的用戶端應用程式提供遠端存取功能。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fa7c2-134">遠端存取服務管理</span><span class="sxs-lookup"><span data-stu-id="fa7c2-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="fa7c2-135">遠端存取服務管理提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="fa7c2-136">您可以使用這些函數開發 RAS 伺服器管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa7c2-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fa7c2-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa7c2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa7c2-138">路由</span><span class="sxs-lookup"><span data-stu-id="fa7c2-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="fa7c2-139">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="fa7c2-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





