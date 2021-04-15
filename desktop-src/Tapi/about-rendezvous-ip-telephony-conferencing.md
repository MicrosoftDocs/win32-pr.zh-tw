---
description: TAPI 3 會合控制項提供了用來通告及探索多方多媒體 IP 會議的機制。 以下描述一組元件物件模型 (COM) 元件和介面來執行會議。
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: 關於會合 IP 電話語音會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554028"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="1cb4a-104">關於會合 IP 電話語音會議</span><span class="sxs-lookup"><span data-stu-id="1cb4a-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="1cb4a-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1cb4a-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1cb4a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1cb4a-107">TAPI 3 會合控制項提供了用來通告及探索多方多媒體 IP 會議的機制。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="1cb4a-108">以下描述一組元件物件模型 (COM) 元件和介面來執行會議。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="1cb4a-109">COM 是適用于 TAPI 3 的基本程式碼模型，在本檔中，我們會假設您已熟悉。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="1cb4a-110">如需 COM 的詳細資訊，請搜尋平臺軟體發展工具組 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="1cb4a-111">功能</span><span class="sxs-lookup"><span data-stu-id="1cb4a-111">Features</span></span>

-   <span data-ttu-id="1cb4a-112">提供會議目錄的摘要，以操作多媒體會議的公告</span><span class="sxs-lookup"><span data-stu-id="1cb4a-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="1cb4a-113">透過驗證、加密及每個公告存取控制層 (ACL 提供安全性) </span><span class="sxs-lookup"><span data-stu-id="1cb4a-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="1cb4a-114">提供會議公告的一般架構，並依屬性值啟用搜尋</span><span class="sxs-lookup"><span data-stu-id="1cb4a-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="1cb4a-115">允許延伸模組透過提供者維護的屬性 (架構中的會議 blob) </span><span class="sxs-lookup"><span data-stu-id="1cb4a-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="1cb4a-116">提供多播位址配置的 COM 包裝函式， (MADCAP) API</span><span class="sxs-lookup"><span data-stu-id="1cb4a-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="1cb4a-117">架構</span><span class="sxs-lookup"><span data-stu-id="1cb4a-117">Architecture</span></span>

<span data-ttu-id="1cb4a-118">下列說明和圖表說明系統架構的重要層面。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="1cb4a-119">用戶端可以使用會合控制項來操作儲存在 ILS 動態目錄或 NTDS 伺服器上的會議。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="1cb4a-120">輕量型目錄存取協定 (LDAP) 用來與 ILS 伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="1cb4a-121">會合控制項提供用於腳本和程式設計的雙重 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="1cb4a-122">會話公告通訊協定 (可直接存取網際網路的 SAP) 伺服器會接聽網際網路上的會議公告，並以會議資訊填入 ILS 動態伺服器。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="1cb4a-123">同樣地，它也會宣佈在本機建立的會議範圍包含網際網路。</span><span class="sxs-lookup"><span data-stu-id="1cb4a-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="1cb4a-124"> (不會針對 Microsoft Windows 2000 規劃 SAP 伺服器。 ) </span><span class="sxs-lookup"><span data-stu-id="1cb4a-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![會合系統架構](images/rend1.png)

 

 



