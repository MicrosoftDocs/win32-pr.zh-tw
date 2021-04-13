---
description: IUpdateService 介面會定義下列屬性。
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: IUpdateService 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469152"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="60356-103">IUpdateService 屬性</span><span class="sxs-lookup"><span data-stu-id="60356-103">IUpdateService Properties</span></span>

<span data-ttu-id="60356-104">[**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="60356-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="60356-105">屬性</span><span class="sxs-lookup"><span data-stu-id="60356-105">Property</span></span>                                                              | <span data-ttu-id="60356-106">描述</span><span class="sxs-lookup"><span data-stu-id="60356-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60356-107">**CanRegisterWithAU**</span><span class="sxs-lookup"><span data-stu-id="60356-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="60356-108">取得布林值，這個值會指出服務是否可以向自動更新註冊。</span><span class="sxs-lookup"><span data-stu-id="60356-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="60356-109">**ContentValidationCert**</span><span class="sxs-lookup"><span data-stu-id="60356-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="60356-110">取得用來簽署服務內容之憑證的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="60356-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="60356-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="60356-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="60356-112">取得授權封包檔到期的日期。</span><span class="sxs-lookup"><span data-stu-id="60356-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="60356-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="60356-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="60356-114">取得布林值，指出服務是否為 managed 服務。</span><span class="sxs-lookup"><span data-stu-id="60356-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="60356-115">**IsRegisteredWithAU**</span><span class="sxs-lookup"><span data-stu-id="60356-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="60356-116">取得布林值，這個值會指出服務是否已向自動更新註冊。</span><span class="sxs-lookup"><span data-stu-id="60356-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="60356-117">**IsScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="60356-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="60356-118">取得布林值，指出服務是否以掃描封裝為基礎。</span><span class="sxs-lookup"><span data-stu-id="60356-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="60356-119">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="60356-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="60356-120">取得授權封包檔的發出日期。</span><span class="sxs-lookup"><span data-stu-id="60356-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="60356-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="60356-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="60356-122">取得服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="60356-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="60356-123">**OffersWindowsUpdates**</span><span class="sxs-lookup"><span data-stu-id="60356-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="60356-124">取得布林值，指出目前的服務是否提供來自 Windows Update 的更新。</span><span class="sxs-lookup"><span data-stu-id="60356-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="60356-125">**RedirectUrls**</span><span class="sxs-lookup"><span data-stu-id="60356-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="60356-126">取得重新導向程式封包檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="60356-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="60356-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="60356-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="60356-128">取得服務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="60356-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="60356-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="60356-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="60356-130">取得服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="60356-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="60356-131">**SetupPrefix**</span><span class="sxs-lookup"><span data-stu-id="60356-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="60356-132">取得安裝檔的前置詞。</span><span class="sxs-lookup"><span data-stu-id="60356-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



