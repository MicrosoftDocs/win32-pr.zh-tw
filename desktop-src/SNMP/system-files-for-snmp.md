---
title: SNMP 的系統檔案
description: 下表說明與 SNMP 服務相關的主要檔案。
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462136"
---
# <a name="system-files-for-snmp"></a><span data-ttu-id="6c9c4-103">SNMP 的系統檔案</span><span class="sxs-lookup"><span data-stu-id="6c9c4-103">System Files for SNMP</span></span>

<span data-ttu-id="6c9c4-104">下表說明與 SNMP 服務相關的主要檔案。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-104">The following table describes the principal files that relate to the SNMP service.</span></span>



| <span data-ttu-id="6c9c4-105">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="6c9c4-105">Filename</span></span>     | <span data-ttu-id="6c9c4-106">描述</span><span class="sxs-lookup"><span data-stu-id="6c9c4-106">Description</span></span>                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9c4-107">DHCPMIB.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-107">DHCPMIB.DLL</span></span>  | <span data-ttu-id="6c9c4-108">可執行 Microsoft 定義之 DHCP MIB 的擴充代理程式 DLL。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-108">Extension agent DLL that implements the Microsoft-defined DHCP MIB.</span></span> <span data-ttu-id="6c9c4-109">只安裝在 DHCP 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-109">Installed only on DHCP servers.</span></span>                                                                                                                                 |
| <span data-ttu-id="6c9c4-110">EVNTAGNT.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-110">EVNTAGNT.DLL</span></span> | <span data-ttu-id="6c9c4-111">將事件記錄檔轉譯為 SNMP 陷阱的 SNMP DLL;也稱為 SNMP 事件轉譯程式。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-111">SNMP DLL that translates event logs into SNMP traps; also known as the SNMP event translator.</span></span>                                                                                                                                       |
| <span data-ttu-id="6c9c4-112">HOSTMIB.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-112">HOSTMIB.DLL</span></span>  | <span data-ttu-id="6c9c4-113">執行主機資源 MIB 的擴充代理程式 DLL。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-113">Extension agent DLL that implements the Host Resources MIB.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="6c9c4-114">LMMIB2.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-114">LMMIB2.DLL</span></span>   | <span data-ttu-id="6c9c4-115">執行 LAN Manager MIB-II 的擴充代理程式 DLL。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-115">Extension agent DLL that implements LAN Manager MIB-II.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="6c9c4-116">MGMTAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-116">MGMTAPI.DLL</span></span>  | <span data-ttu-id="6c9c4-117">Microsoft SNMP 管理 API 程式庫。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-117">Microsoft SNMP Management API library.</span></span> <span data-ttu-id="6c9c4-118">此 API 可讓 SNMP 管理員應用程式「接聽」 SNMP 管理員要求，並將要求傳送至 SNMP 代理程式並接收回應。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-118">This API allows SNMP manager applications to "listen" for SNMP manager requests, and send requests to and receive responses from SNMP agents.</span></span>                                                |
| <span data-ttu-id="6c9c4-119">Mib。站</span><span class="sxs-lookup"><span data-stu-id="6c9c4-119">MIB.BIN</span></span>      | <span data-ttu-id="6c9c4-120">MGMTAPI.DLL 所使用的已編譯 MIB 資訊。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-120">Compiled MIB information used by MGMTAPI.DLL.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="6c9c4-121">SNMP.EXE</span><span class="sxs-lookup"><span data-stu-id="6c9c4-121">SNMP.EXE</span></span>     | <span data-ttu-id="6c9c4-122">SNMP 服務。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-122">SNMP service.</span></span> <span data-ttu-id="6c9c4-123">這是接收 SNMP 要求並將其傳遞至適當擴充代理程式 DLL 的主要代理程式。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-123">This is the master agent that receives SNMP requests and delivers them to the appropriate extension agent DLL.</span></span>                                                                                                        |
| <span data-ttu-id="6c9c4-124">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-124">SNMPAPI.DLL</span></span>  | <span data-ttu-id="6c9c4-125">Snmp 公用程式 DLL （snmp）擴充代理程式 Dll 和管理員應用程式所使用的 DLL。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-125">SNMP utilities DLL used by SNMP extension agent DLLs and manager applications.</span></span> <span data-ttu-id="6c9c4-126">此 DLL 包含開發延伸模組代理程式 Dll 的架構。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-126">This DLL contains a framework for developing extension agent DLLs.</span></span>                                                                                   |
| <span data-ttu-id="6c9c4-127">SNMPSNAP.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-127">SNMPSNAP.DLL</span></span> | <span data-ttu-id="6c9c4-128">SNMP 設定應用程式，也就是 (MMC) 嵌入式管理單元元件的 Microsoft Management Console。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-128">SNMP configuration application that is a Microsoft Management Console (MMC) snap-in component.</span></span> <span data-ttu-id="6c9c4-129">此嵌入式管理單元會將數個頁面新增至 SNMP 服務的 [內容] 工作表。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-129">The snap-in adds several pages to the SNMP Service Properties sheet.</span></span> <span data-ttu-id="6c9c4-130">如需詳細資訊，請參閱 SNMP 服務的線上說明。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-130">For more information, see the online help for the SNMP service.</span></span> |
| <span data-ttu-id="6c9c4-131">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="6c9c4-131">SNMPTRAP.EXE</span></span> | <span data-ttu-id="6c9c4-132">SNMP 陷阱服務。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-132">SNMP trap service.</span></span> <span data-ttu-id="6c9c4-133">接收 SNMP 陷阱，並將其轉送到 SNMP 管理員應用程式。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-133">Receives SNMP traps and forwards them to SNMP manager applications.</span></span>                                                                                                                                              |
| <span data-ttu-id="6c9c4-134">WINSMIB.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-134">WINSMIB.DLL</span></span>  | <span data-ttu-id="6c9c4-135">擴充代理程式 DLL，可執行 Microsoft 定義的 WINS MIB。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-135">Extension agent DLL that implements the Microsoft-defined WINS MIB.</span></span> <span data-ttu-id="6c9c4-136">只安裝在 WINS 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-136">Installed only on WINS servers.</span></span>                                                                                                                                 |
| <span data-ttu-id="6c9c4-137">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="6c9c4-137">WSNMP32.DLL</span></span>  | <span data-ttu-id="6c9c4-138">Microsoft [WINSNMP API](winsnmp-api.md) 程式庫。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-138">Microsoft [WinSNMP API](winsnmp-api.md) library.</span></span> <span data-ttu-id="6c9c4-139">此 API 可讓 SNMP 管理員應用程式「接聽」 SNMP 管理員要求，並將要求傳送至 SNMP 代理程式並接收回應。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-139">This API allows SNMP manager applications to "listen" for SNMP manager requests, and send requests to and receive responses from SNMP agents.</span></span>                                     |



 

<span data-ttu-id="6c9c4-140">如需詳細資訊，請參閱 [SNMP 管理資訊基礎 (MIB) ](the-snmp-management-information-base-mib-.md)。</span><span class="sxs-lookup"><span data-stu-id="6c9c4-140">For additional information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md).</span></span> <span data-ttu-id="6c9c4-141"> (您也可以參考 Windows 2000 資源套件。 ) </span><span class="sxs-lookup"><span data-stu-id="6c9c4-141">(You can also refer to the Windows 2000 Resource Kit.)</span></span>

 

 




