---
title: 關於 EAP
description: 可延伸的驗證通訊協定 (EAP) ，這是許多 Microsoft 網路元件所支援的標準。
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- 可延伸的驗證通訊協定，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383097"
---
# <a name="about-eap"></a><span data-ttu-id="55900-104">關於 EAP</span><span class="sxs-lookup"><span data-stu-id="55900-104">About EAP</span></span>

<span data-ttu-id="55900-105">本主題說明可延伸的驗證通訊協定 (EAP) ，這是許多 Microsoft 網路元件所支援的標準。</span><span class="sxs-lookup"><span data-stu-id="55900-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="55900-106">EAP 元件</span><span class="sxs-lookup"><span data-stu-id="55900-106">EAP Components</span></span>

<span data-ttu-id="55900-107">EAP 對於保護無線 (802.1 X) Lan、有線區域網路以及撥號和虛擬私人網路 (Vpn) 的安全性非常重要。</span><span class="sxs-lookup"><span data-stu-id="55900-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="55900-108">下列元件支援 EAP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="55900-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="55900-109">適用于撥號和 VPN 的 Microsoft 遠端存取用戶端和伺服器 (PPTP 和 L2TP/IPSec) 將 EAP 實作為 PPP 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="55900-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="55900-110">如需詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063)。</span><span class="sxs-lookup"><span data-stu-id="55900-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="55900-111">Microsoft IEEE 802.1 X 相容的無線和有線區域網路客戶會依照 IEEE 802.1 X draft 標準的定義來實行 EAP。</span><span class="sxs-lookup"><span data-stu-id="55900-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="55900-112">Microsoft RADIUS 伺服器稱為網際網路驗證服務 (IAS) 依照 [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055)中的定義來實行 EAP。</span><span class="sxs-lookup"><span data-stu-id="55900-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="55900-113">上述所有元件都支援透過 Microsoft Windows 軟體開發套件 (SDK) 的可延伸架構，讓您可以整合協力廠商驗證模組。</span><span class="sxs-lookup"><span data-stu-id="55900-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="55900-114">這種可延伸的機制可用來支援權杖卡、Kerberos、公開金鑰和 S/金鑰驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="55900-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="55900-115">受保護的可延伸驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="55900-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="55900-116">除了 EAP 之外，無線 (802.1 X) 實行和 RADIUS 伺服器也支援稱為受保護 EAP (PEAP) 的新興標準。</span><span class="sxs-lookup"><span data-stu-id="55900-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="55900-117">PEAP 提供許多重要服務給其他 EAP 驗證通訊協定，如下所示。</span><span class="sxs-lookup"><span data-stu-id="55900-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="55900-118">PEAP 使用傳輸層安全性 (TLS) （ (SSL) 型技術的安全通訊端層），來加密其他 EAP 驗證通訊協定的 EAP 封包。</span><span class="sxs-lookup"><span data-stu-id="55900-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="55900-119">如需詳細資訊，請參閱 [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050)。</span><span class="sxs-lookup"><span data-stu-id="55900-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="55900-120">PEAP 使用伺服器憑證來驗證服務器端與 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="55900-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="55900-121">PEAP 提供快速的重新驗證功能，可支援在無線裝置之間進行有效率的漫遊。</span><span class="sxs-lookup"><span data-stu-id="55900-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="55900-122">PEAP 管理分散和重新組裝 EAP 封包。</span><span class="sxs-lookup"><span data-stu-id="55900-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="55900-123">PEAP 會產生用來加密無線流量的金鑰。</span><span class="sxs-lookup"><span data-stu-id="55900-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="55900-124">PEAP 讓撰寫 EAP 通訊協定更加容易，因為程式設計師不再需要解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="55900-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55900-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="55900-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55900-126">關於 EAP 和 EAPHost</span><span class="sxs-lookup"><span data-stu-id="55900-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




