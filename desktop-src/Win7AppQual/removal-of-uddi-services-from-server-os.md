---
description: 從伺服器作業系統移除 UDDI 服務
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: 從伺服器作業系統移除 UDDI 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116326"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="1eeb2-103">從伺服器作業系統移除 UDDI 服務</span><span class="sxs-lookup"><span data-stu-id="1eeb2-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="1eeb2-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="1eeb2-104">Affected Platform</span></span>

<span data-ttu-id="1eeb2-105">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1eeb2-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="1eeb2-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="1eeb2-106">Feature Impact</span></span>

<span data-ttu-id="1eeb2-107">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="1eeb2-107">**Severity** - Medium</span></span>  
<span data-ttu-id="1eeb2-108">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="1eeb2-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="1eeb2-109">Description</span><span class="sxs-lookup"><span data-stu-id="1eeb2-109">Description</span></span>

<span data-ttu-id="1eeb2-110">Microsoft 已從 Windows Server 2008 R2 移除 UDDI (通用描述、探索與整合) 服務伺服器角色。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="1eeb2-111">未來的 UDDI 服務版本將會是 Microsoft BizTalk 產品的一部分。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="1eeb2-112">這種產品重做和匯總可定位 Microsoft，以提供服務導向架構 (SOA) 市場。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="1eeb2-113">「UDDI 服務」的第一版 Windows Server 2008 版將會符合「UDDI v3.0 標準」。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="1eeb2-114">它會隨附于 BizTalk Server 2009 版本中。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="1eeb2-115">為了符合我們的承諾，提供令人滿意的使用者體驗，我們將提供適用于 Windows Server 2008 R2 的 UDDI 服務 v3 安裝套件。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="1eeb2-116">表現</span><span class="sxs-lookup"><span data-stu-id="1eeb2-116">Manifestation</span></span>

<span data-ttu-id="1eeb2-117">如果系統上有舊版的 UDDI 服務元件，則會封鎖升級至 Windows Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="1eeb2-118">影響緩和措施</span><span class="sxs-lookup"><span data-stu-id="1eeb2-118">Mitigation of Impact</span></span>

<span data-ttu-id="1eeb2-119">從 Windows Server 2003 或 Windows Server 2008 部署「UDDI 服務」網站的使用者可以選擇不要將執行「UDDI 服務」的伺服器升級為 Windows Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="1eeb2-120">如果他們必須升級目前的「UDDI 服務」方塊，也可以將「UDDI 服務」移至專用的 Windows Server 2003 或 Windows Server 2008 方塊。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="1eeb2-121">解決方法</span><span class="sxs-lookup"><span data-stu-id="1eeb2-121">Solution</span></span>

<span data-ttu-id="1eeb2-122">建議的解決方法是將 UDDI 服務 v3.0 從 BizTalk Server 2009 部署到 Windows Server 2008 R2 電腦，然後將舊的網站遷移到新的網站。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="1eeb2-123">UDDI 服務 v3.0 提供與 UDDI 服務2.0 的回溯相容性，因此任何使用 UDDI 服務的應用程式都不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="1eeb2-124">若要這樣做，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1eeb2-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="1eeb2-125">在已載入 Windows Server 2008 R2 的電腦上設定新的 UDDI 服務 v3.0 網站。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="1eeb2-126"> (注意：在分散式安裝中，UDDI v3.0 網站可由一個以上的 Windows Server 2008 R2 電腦群組成。 ) </span><span class="sxs-lookup"><span data-stu-id="1eeb2-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="1eeb2-127">使用 UDDI 資料移轉工具，將舊的「UDDI 服務」資料庫中的資料移轉至新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="1eeb2-128">備份舊的 UDDI 服務資料庫，以確保復原功能。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="1eeb2-129">卸載舊的「UDDI 服務」軟體，然後將這些方塊升級至 Windows Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="1eeb2-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1eeb2-130">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="1eeb2-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="1eeb2-131">Microsoft UDDI 服務網站</span><span class="sxs-lookup"><span data-stu-id="1eeb2-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="1eeb2-132">UDDI 規格</span><span class="sxs-lookup"><span data-stu-id="1eeb2-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="1eeb2-133">適用于 Windows Server 2008 R2 的 UDDI 服務 v3.0 下載</span><span class="sxs-lookup"><span data-stu-id="1eeb2-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



