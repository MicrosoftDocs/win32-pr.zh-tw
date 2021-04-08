---
title: 網路存取保護
description: 請注意，從 Windows 10 網路存取保護開始，無法使用網路存取保護平臺 (NAP) 是一組作業系統元件，可提供保護私人網路存取的平臺。
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- 網路存取保護
- 網路存取保護，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672735"
---
# <a name="network-access-protection"></a><span data-ttu-id="8070e-105">網路存取保護</span><span class="sxs-lookup"><span data-stu-id="8070e-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="8070e-106">目的</span><span class="sxs-lookup"><span data-stu-id="8070e-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="8070e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8070e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8070e-108">網路存取保護 (NAP) 是一組作業系統元件，可提供保護私人網路存取的平臺。</span><span class="sxs-lookup"><span data-stu-id="8070e-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="8070e-109">NAP 平臺提供了一種整合方式，可評估網路用戶端的系統健全狀況狀態，嘗試連線到網路或在網路上通訊，以及限制網路用戶端的存取，直到達到健康原則需求為止。</span><span class="sxs-lookup"><span data-stu-id="8070e-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="8070e-110">NAP 是可延伸的平臺，可提供基礎結構和 API 集，以新增儲存、報告、驗證和修正電腦系統健全狀態的元件。</span><span class="sxs-lookup"><span data-stu-id="8070e-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="8070e-111">NAP 平臺本身不會提供元件來累積和評估電腦健全狀況狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="8070e-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="8070e-112">其他元件（稱為系統健康狀態代理程式） (Sha) 和系統健康狀態驗證 (Shv) ，可提供網路原則驗證和網路原則合規性。</span><span class="sxs-lookup"><span data-stu-id="8070e-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8070e-113">適用時</span><span class="sxs-lookup"><span data-stu-id="8070e-113">Where applicable</span></span>

<span data-ttu-id="8070e-114">NAP 是設計成可擴充的。</span><span class="sxs-lookup"><span data-stu-id="8070e-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="8070e-115">它可以與任何提供 Sha 和 Shv 或辨識其已發佈 API 集的廠商軟體交互操作。</span><span class="sxs-lookup"><span data-stu-id="8070e-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="8070e-116">NAP 有助於提供適用于下列常見案例的解決方案：</span><span class="sxs-lookup"><span data-stu-id="8070e-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="8070e-117">檢查漫遊膝上型電腦的健康情況和狀態。</span><span class="sxs-lookup"><span data-stu-id="8070e-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="8070e-118">確定桌上型電腦的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="8070e-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="8070e-119">確認遠端辦公室電腦的相容性和健康情況。</span><span class="sxs-lookup"><span data-stu-id="8070e-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="8070e-120">判斷造訪筆記本電腦的健康情況。</span><span class="sxs-lookup"><span data-stu-id="8070e-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="8070e-121">確認未受管理的家用電腦的相容性和健康情況。</span><span class="sxs-lookup"><span data-stu-id="8070e-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8070e-122">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8070e-122">Developer audience</span></span>

<span data-ttu-id="8070e-123">NAP API 是針對 C/c + + 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="8070e-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="8070e-124">針對 NAP 強制方法，程式設計人員應該熟悉網路通訊協定和技術，例如遠端驗證撥入使用者服務 (RADIUS) 、動態主機設定通訊協定 (DHCP) 、虛擬私人網路 (Vpn) 、有線和無線存取的 IEEE 802.1 X 標準，以及網際網路通訊協定安全性 (IPsec) 。</span><span class="sxs-lookup"><span data-stu-id="8070e-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8070e-125">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8070e-125">Run-time requirements</span></span>

<span data-ttu-id="8070e-126">NAP 平臺需要執行 Windows Server 2008 或更新版本的 nap 基礎結構伺服器，以及執行 Windows XP Service Pack 3 (SP3) 、Windows Vista 或更新版本作業系統的 NAP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="8070e-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="8070e-127">如需哪些作業系統支援特定程式設計專案的特定資訊，請參閱 NAP 參考檔中 NAP Api 的需求章節。</span><span class="sxs-lookup"><span data-stu-id="8070e-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8070e-128">本節內容</span><span class="sxs-lookup"><span data-stu-id="8070e-128">In this section</span></span>



| <span data-ttu-id="8070e-129">主題</span><span class="sxs-lookup"><span data-stu-id="8070e-129">Topic</span></span>                                         | <span data-ttu-id="8070e-130">描述</span><span class="sxs-lookup"><span data-stu-id="8070e-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="8070e-131">關於 NAP</span><span class="sxs-lookup"><span data-stu-id="8070e-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="8070e-132">NAP API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="8070e-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="8070e-133">使用 NAP</span><span class="sxs-lookup"><span data-stu-id="8070e-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="8070e-134">NAP API 的使用範例。</span><span class="sxs-lookup"><span data-stu-id="8070e-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="8070e-135">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="8070e-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="8070e-136">NAP 介面、結構和其他程式碼元素的檔。</span><span class="sxs-lookup"><span data-stu-id="8070e-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





