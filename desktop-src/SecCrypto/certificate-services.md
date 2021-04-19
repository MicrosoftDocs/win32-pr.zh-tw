---
description: 憑證服務是在 Windows server 作業系統上執行的服務，會接收透過傳輸（例如 RPC 或 HTTP）的新數位憑證要求。
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: 憑證服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998521"
---
# <a name="certificate-services"></a><span data-ttu-id="93928-103">憑證服務</span><span class="sxs-lookup"><span data-stu-id="93928-103">Certificate Services</span></span>

<span data-ttu-id="93928-104">[*憑證服務*](../secgloss/c-gly.md)是在 Windows server 作業系統上執行的服務，會接收透過傳輸（例如 RPC 或 HTTP）的新數位憑證要求。</span><span class="sxs-lookup"><span data-stu-id="93928-104">[*Certificate Services*](../secgloss/c-gly.md), a service running on a Windows server operating system, receives requests for new digital certificates over transports such as RPC or HTTP.</span></span> <span data-ttu-id="93928-105">它會根據自訂或網站特定原則來檢查每個要求、設定要發行之憑證的選擇性屬性，以及頒發證書。</span><span class="sxs-lookup"><span data-stu-id="93928-105">It checks each request against custom or site-specific policies, sets optional properties for a certificate to be issued, and issues the certificate.</span></span> <span data-ttu-id="93928-106">憑證服務可讓系統管理員將專案新增至 (CRL) 的 [*憑證撤銷清單*](../secgloss/c-gly.md) ，以及定期發佈已簽署的 crl。</span><span class="sxs-lookup"><span data-stu-id="93928-106">Certificate Services allows administrators to add elements to a [*certificate revocation list*](../secgloss/c-gly.md) (CRL), and to publish signed CRLs on a regular basis.</span></span>

<span data-ttu-id="93928-107">憑證服務包含可程式化的介面，可用於建立其他傳輸、原則和憑證屬性與格式的支援。</span><span class="sxs-lookup"><span data-stu-id="93928-107">Certificate services include programmable interfaces for creating support for additional transports, policies, and certificate properties and formats.</span></span>

<span data-ttu-id="93928-108">在 Windows Server 2003 中，您可以按一下 [**新增或移除程式**]，然後按一下 [**新增/移除 Windows 元件**] 以安裝或卸載憑證服務，從 **主控台** 安裝憑證服務2.0。</span><span class="sxs-lookup"><span data-stu-id="93928-108">In Windows Server 2003, Certificate Services 2.0 can be installed from **Control Panel** by clicking **Add or Remove Programs** and then clicking **Add/Remove Windows Components** to install or uninstall Certificate Services.</span></span>

<span data-ttu-id="93928-109">下列各節將詳細說明憑證服務概念。</span><span class="sxs-lookup"><span data-stu-id="93928-109">Certificate Services concepts are detailed in the following sections.</span></span> <span data-ttu-id="93928-110">內容旨在協助您開發會與憑證服務互動的應用程式。</span><span class="sxs-lookup"><span data-stu-id="93928-110">The content is intended to help you develop applications that will interact with Certificate Services.</span></span>



| <span data-ttu-id="93928-111">Content</span><span class="sxs-lookup"><span data-stu-id="93928-111">Content</span></span>                                                                                                                                                           | <span data-ttu-id="93928-112">區段</span><span class="sxs-lookup"><span data-stu-id="93928-112">Section</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="93928-113">憑證服務功能的描述</span><span class="sxs-lookup"><span data-stu-id="93928-113">Description of the features of Certificate Services</span></span>                                                                                                               | [<span data-ttu-id="93928-114">憑證服務功能</span><span class="sxs-lookup"><span data-stu-id="93928-114">Certificate Services Features</span></span>](certificate-services-features.md)         |
| <span data-ttu-id="93928-115">憑證服務架構的總覽</span><span class="sxs-lookup"><span data-stu-id="93928-115">Overview of Certificate Services architecture</span></span>                                                                                                                     | [<span data-ttu-id="93928-116">憑證服務架構</span><span class="sxs-lookup"><span data-stu-id="93928-116">Certificate Services Architecture</span></span>](certificate-services-architecture.md) |
| <span data-ttu-id="93928-117">憑證、憑證主體和主體公開金鑰之間的關聯性[ ](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="93928-117">Relationship between a certificate, the certificate's subject, and the subject's [*public key*](../secgloss/p-gly.md)</span></span> | [<span data-ttu-id="93928-118">憑證和公開金鑰</span><span class="sxs-lookup"><span data-stu-id="93928-118">Certificates and Public Keys</span></span>](certificates-and-public-keys.md)           |
| <span data-ttu-id="93928-119">憑證要求屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="93928-119">Information about the Certificate Request properties</span></span>                                                                                                              | [<span data-ttu-id="93928-120">憑證要求指導方針</span><span class="sxs-lookup"><span data-stu-id="93928-120">Certificate Request Guidelines</span></span>](certificate-request-guidelines.md)       |
| <span data-ttu-id="93928-121">憑證服務處理憑證方式的詳細資料</span><span class="sxs-lookup"><span data-stu-id="93928-121">Details of how a certificate is processed by Certificate Services</span></span>                                                                                                 | [<span data-ttu-id="93928-122">關於憑證</span><span class="sxs-lookup"><span data-stu-id="93928-122">About Certificates</span></span>](about-certificates.md)                               |
| <span data-ttu-id="93928-123">[*憑證授權單位*](../secgloss/c-gly.md)單位更新程式的描述</span><span class="sxs-lookup"><span data-stu-id="93928-123">Description of the [*certification authority*](../secgloss/c-gly.md) renewal process</span></span>        | [<span data-ttu-id="93928-124">憑證授權單位單位更新</span><span class="sxs-lookup"><span data-stu-id="93928-124">Certification Authority Renewal</span></span>](certification-authority-renewal.md)     |



 

<span data-ttu-id="93928-125">另外也包含下列其他有用的主題。</span><span class="sxs-lookup"><span data-stu-id="93928-125">The following additional useful topics are also included.</span></span>



| <span data-ttu-id="93928-126">Content</span><span class="sxs-lookup"><span data-stu-id="93928-126">Content</span></span>                                                                                                                                             | <span data-ttu-id="93928-127">區段</span><span class="sxs-lookup"><span data-stu-id="93928-127">Section</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="93928-128">憑證註冊控制項的相關檔，提供用來建立憑證要求的服務，包括智慧卡使用者的要求。</span><span class="sxs-lookup"><span data-stu-id="93928-128">Documentation on Certificate Enrollment Control, which provides services for creating certificate requests including requests for smart card users.</span></span> | [<span data-ttu-id="93928-129">憑證註冊控制項</span><span class="sxs-lookup"><span data-stu-id="93928-129">Certificate Enrollment Control</span></span>](certificate-enrollment-control.md) |
| <span data-ttu-id="93928-130">Microsoft 密碼編譯應用程式開發介面的檔，可提供密碼編譯式安全性服務。</span><span class="sxs-lookup"><span data-stu-id="93928-130">Documentation on the Microsoft Cryptographic Application Programming Interface, which provides cryptography-based security services.</span></span>                | [<span data-ttu-id="93928-131">密碼編譯基本概念</span><span class="sxs-lookup"><span data-stu-id="93928-131">Cryptography Essentials</span></span>](cryptography-essentials.md)               |
| <span data-ttu-id="93928-132">智慧卡上的檔，提供用於開發和使用智慧卡系統的服務。</span><span class="sxs-lookup"><span data-stu-id="93928-132">Documentation on Smart Card, which provides services for developing and using smart card systems.</span></span>                                                   | [<span data-ttu-id="93928-133">智慧卡</span><span class="sxs-lookup"><span data-stu-id="93928-133">Smart Card</span></span>](../secauthn/smart-card-authentication.md)                     |
| <span data-ttu-id="93928-134">憑證和憑證要求的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="93928-134">Name properties of certificates and certificate requests.</span></span>                                                                                           | [<span data-ttu-id="93928-135">名稱屬性</span><span class="sxs-lookup"><span data-stu-id="93928-135">Name Properties</span></span>](name-properties.md)                               |
| <span data-ttu-id="93928-136">[*X.509*](../secgloss/x-gly.md)憑證屬性的清單和描述。</span><span class="sxs-lookup"><span data-stu-id="93928-136">List and descriptions of [*X.509*](../secgloss/x-gly.md) certificate properties.</span></span>                                  | [<span data-ttu-id="93928-137">憑證屬性</span><span class="sxs-lookup"><span data-stu-id="93928-137">Certificate Properties</span></span>](certificate-properties.md)                 |



 

 

 
