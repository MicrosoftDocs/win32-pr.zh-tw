---
title: 可延伸的驗證通訊協定
description: 可延伸的驗證通訊協定 (EAP) 是數個系統元件所支援的標準。 EAP 對於保護無線 (802.1 X) 和有線區域網路、撥號和虛擬私人網路 (Vpn) 的安全性非常重要。
ms.assetid: bdbac41e-064c-445f-8f86-a6e2eff2a683
keywords:
- 可延伸的驗證通訊協定
- 可延伸的驗證通訊協定，起始頁
- EAP
- EAP，請參閱可延伸的驗證通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79b9585363d74eb50190d0fd6355830a7087aa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681767"
---
# <a name="extensible-authentication-protocol"></a><span data-ttu-id="04f6c-108">可延伸的驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="04f6c-108">Extensible Authentication Protocol</span></span>

## <a name="purpose"></a><span data-ttu-id="04f6c-109">目的</span><span class="sxs-lookup"><span data-stu-id="04f6c-109">Purpose</span></span>

<span data-ttu-id="04f6c-110">可延伸的驗證通訊協定 (EAP) 是數個系統元件所支援的標準。</span><span class="sxs-lookup"><span data-stu-id="04f6c-110">The Extensible Authentication Protocol (EAP) is a standard supported by several system components.</span></span> <span data-ttu-id="04f6c-111">EAP 對於保護無線 (802.1 X) 和有線區域網路、撥號和虛擬私人網路 (Vpn) 的安全性非常重要。</span><span class="sxs-lookup"><span data-stu-id="04f6c-111">EAP is crucial for protecting the security of wireless (802.1X) and wired LANs, Dial-up, and Virtual Private Networks (VPNs).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="04f6c-112">適用時</span><span class="sxs-lookup"><span data-stu-id="04f6c-112">Where applicable</span></span>

<span data-ttu-id="04f6c-113">EAP 改進了先前的驗證通訊協定，例如密碼驗證通訊協定 (PAP) 和挑戰交握驗證通訊協定 (CHAP) 。</span><span class="sxs-lookup"><span data-stu-id="04f6c-113">EAP improves on previous authentication protocols such as Password Authentication Protocol (PAP) and Challenge Handshake Authentication Protocol (CHAP).</span></span>

<span data-ttu-id="04f6c-114">如需新的 EAP 方法開發，請參閱可延伸的 [驗證通訊協定主機](../eaphost/portal.md)。</span><span class="sxs-lookup"><span data-stu-id="04f6c-114">For new EAP method development, see [Extensible Authentication Protocol Host](../eaphost/portal.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04f6c-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="04f6c-115">Developer audience</span></span>

<span data-ttu-id="04f6c-116">EAP API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="04f6c-116">The EAP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="04f6c-117">程式設計人員應該熟悉網路概念。</span><span class="sxs-lookup"><span data-stu-id="04f6c-117">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04f6c-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="04f6c-118">Run-time requirements</span></span>

<span data-ttu-id="04f6c-119">在 Windows 2000 和更新版本上執行的用戶端和伺服器電腦都支援 EAP。</span><span class="sxs-lookup"><span data-stu-id="04f6c-119">EAP is supported on client and server computers running on  Windows 2000 and later.</span></span> <span data-ttu-id="04f6c-120">在 Windows 2000 Server 和更新版本上執行的電腦上也支援 EAP，如果它們正在 (IAS) 執行網際網路驗證服務。</span><span class="sxs-lookup"><span data-stu-id="04f6c-120">EAP is also supported on computers running on Windows 2000 Server and later if they are running Internet Authentication Service (IAS).</span></span> <span data-ttu-id="04f6c-121">如需有關支援之作業系統的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="04f6c-121">For more information about supported operating systems, see the Requirements section in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04f6c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="04f6c-122">Related topics</span></span>

<dl> <span data-ttu-id="04f6c-123"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="04f6c-123"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="04f6c-124">遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="04f6c-124">Remote Access Service</span></span>](/windows/desktop/RRAS/remote-access-start-page)
<span data-ttu-id="04f6c-125"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="04f6c-125"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="04f6c-126">網際網路驗證服務</span><span class="sxs-lookup"><span data-stu-id="04f6c-126">Internet Authentication Service</span></span>](/windows/desktop/Nps/ias-extensions)
<span data-ttu-id="04f6c-127"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="04f6c-127"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="04f6c-128">使用可延伸的驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="04f6c-128">Using Extensible Authentication Protocol</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
<span data-ttu-id="04f6c-129"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="04f6c-129"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="04f6c-130">可延伸的驗證通訊協定參考</span><span class="sxs-lookup"><span data-stu-id="04f6c-130">Extensible Authentication Protocol Reference</span></span>](extensible-authentication-protocol-reference.md)
</dt> </dl>

 

 