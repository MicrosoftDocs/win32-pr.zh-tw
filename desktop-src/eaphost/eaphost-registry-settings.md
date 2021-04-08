---
title: EAPHost 登錄設定
description: 下列登錄機碼中的登錄值會控制 EAPHost 功能的各個層面。
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e4d258062ee2ae365924ecda22c2660ed5b742
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841728"
---
# <a name="eaphost-registry-settings"></a><span data-ttu-id="8ccac-103">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="8ccac-103">EAPHost Registry Settings</span></span>

<span data-ttu-id="8ccac-104">下列登錄機碼中的登錄值會控制 EAPHost 功能的各個層面。</span><span class="sxs-lookup"><span data-stu-id="8ccac-104">Registry values in the following registry keys control aspects of the functionality of EAPHost.</span></span>



| <span data-ttu-id="8ccac-105">子機碼</span><span class="sxs-lookup"><span data-stu-id="8ccac-105">Subkey</span></span>                                                                 | <span data-ttu-id="8ccac-106">Description</span><span class="sxs-lookup"><span data-stu-id="8ccac-106">Description</span></span>                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ccac-107">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="8ccac-107">BypassNegotiation</span></span>](bypassnegotiation.md)                             | <span data-ttu-id="8ccac-108">判斷是否發生 RAS 伺服器和用戶端之間的功能協商。</span><span class="sxs-lookup"><span data-stu-id="8ccac-108">Determines if capabilities negotiation between the RAS server and client occurs.</span></span><br/>                                                                              |
| [<span data-ttu-id="8ccac-109">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="8ccac-109">AssumePhase2Fragmentation</span></span>](assumephase2fragmentation.md)             | <span data-ttu-id="8ccac-110">判斷 RAS 伺服器和用戶端是否採用第2階段片段。</span><span class="sxs-lookup"><span data-stu-id="8ccac-110">Determines if the RAS server and client assume phase 2 fragmentation.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8ccac-111">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="8ccac-111">OverrideEAPCertificateSelection</span></span>](overrideeapcertificateselection.md) | <span data-ttu-id="8ccac-112">判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多憑證以供選擇。</span><span class="sxs-lookup"><span data-stu-id="8ccac-112">Determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span><br/> |
| [<span data-ttu-id="8ccac-113">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="8ccac-113">PeapServerUseAllPurposeCert</span></span>](peapserveruseallpurposecert.md)         | <span data-ttu-id="8ccac-114">判斷是否使用所有用途的憑證進行 PEAP 驗證。</span><span class="sxs-lookup"><span data-stu-id="8ccac-114">Determines if all-purpose certificates are used for PEAP authentication.</span></span><br/>                                                                                      |
| [<span data-ttu-id="8ccac-115">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="8ccac-115">PeapServerAcceptAllPurposeCert</span></span>](peapserveracceptallpurposecert.md)   | <span data-ttu-id="8ccac-116">判斷是否接受 PEAP 驗證的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="8ccac-116">Determines if all-purpose certificates are accepted for PEAP authentication.</span></span><br/>                                                                                  |
| [<span data-ttu-id="8ccac-117">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="8ccac-117">TlsServerUseAllPurposeCert</span></span>](tlsserveruseallpurposecert.md)           | <span data-ttu-id="8ccac-118">判斷是否使用所有用途的憑證進行 EAP-TLS 驗證。</span><span class="sxs-lookup"><span data-stu-id="8ccac-118">Determines if all-purpose certificates are used for EAP-TLS authentication.</span></span><br/>                                                                                   |
| [<span data-ttu-id="8ccac-119">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="8ccac-119">TlsServerAcceptAllPurposeCert</span></span>](tlsserveracceptallpurposecert.md)     | <span data-ttu-id="8ccac-120">判斷是否接受 EAP-TLS 驗證的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="8ccac-120">Determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span><br/>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8ccac-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ccac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ccac-122">EAPHost API 參考</span><span class="sxs-lookup"><span data-stu-id="8ccac-122">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 





