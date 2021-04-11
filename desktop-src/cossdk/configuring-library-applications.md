---
description: 設定程式庫應用程式
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: 設定程式庫應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025871"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="b3871-103">設定程式庫應用程式</span><span class="sxs-lookup"><span data-stu-id="b3871-103">Configuring Library Applications</span></span>

<span data-ttu-id="b3871-104">由於 COM + 程式庫應用程式是在用戶端的進程中執行，因此程式庫應用程式的可設定元素與伺服器應用程式的設定元素截然不同。</span><span class="sxs-lookup"><span data-stu-id="b3871-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="b3871-105">您無法設定裝載進程所決定的應用程式任何方面。</span><span class="sxs-lookup"><span data-stu-id="b3871-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="b3871-106">在應用層級中，程式庫應用程式可能會有數個設定受限或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b3871-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="b3871-107">下表說明這些條件約束：</span><span class="sxs-lookup"><span data-stu-id="b3871-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="b3871-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b3871-108">Attribute</span></span>                                       | <span data-ttu-id="b3871-109">描述</span><span class="sxs-lookup"><span data-stu-id="b3871-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3871-110">安全性層級</span><span class="sxs-lookup"><span data-stu-id="b3871-110">Security level</span></span><br/>                       | <span data-ttu-id="b3871-111">您必須選擇元件層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="b3871-111">You must choose component-level access checks.</span></span> <span data-ttu-id="b3871-112">程式庫應用程式無法影響進程層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="b3871-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="b3871-113">請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="b3871-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="b3871-114">啟用或停用驗證</span><span class="sxs-lookup"><span data-stu-id="b3871-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="b3871-115">您可以指定程式庫應用程式是否將參與主機進程所執行的驗證。</span><span class="sxs-lookup"><span data-stu-id="b3871-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="b3871-116">請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。</span><span class="sxs-lookup"><span data-stu-id="b3871-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="b3871-117">模擬等級</span><span class="sxs-lookup"><span data-stu-id="b3871-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="b3871-118">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-118">Unavailable.</span></span> <span data-ttu-id="b3871-119">使用主機進程的設定。</span><span class="sxs-lookup"><span data-stu-id="b3871-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="b3871-120">安全性身分識別</span><span class="sxs-lookup"><span data-stu-id="b3871-120">Security identity</span></span><br/>                    | <span data-ttu-id="b3871-121">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-121">Unavailable.</span></span> <span data-ttu-id="b3871-122">應用程式會在主機進程的身分識別下執行。</span><span class="sxs-lookup"><span data-stu-id="b3871-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="b3871-123">伺服器進程關機</span><span class="sxs-lookup"><span data-stu-id="b3871-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="b3871-124">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b3871-125">啟用 3 GB 支援</span><span class="sxs-lookup"><span data-stu-id="b3871-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="b3871-126">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b3871-127">在偵錯工具中啟動</span><span class="sxs-lookup"><span data-stu-id="b3871-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="b3871-128">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b3871-129">啟用 CRM</span><span class="sxs-lookup"><span data-stu-id="b3871-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="b3871-130">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b3871-131">排隊</span><span class="sxs-lookup"><span data-stu-id="b3871-131">Queuing</span></span><br/>                              | <span data-ttu-id="b3871-132">無法。</span><span class="sxs-lookup"><span data-stu-id="b3871-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="b3871-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3871-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3871-134">COM + 應用程式總覽</span><span class="sxs-lookup"><span data-stu-id="b3871-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




