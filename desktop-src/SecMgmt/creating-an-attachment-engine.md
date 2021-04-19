---
description: 附件引擎是處理服務特定設定和分析要求的 DLL。 換句話說，它會處理標準安全性設定工具集無法處理的處理。
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: 建立附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b16e768956e61fe76406777da2bce9affbfa2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984995"
---
# <a name="creating-an-attachment-engine"></a><span data-ttu-id="0bd51-104">建立附件引擎</span><span class="sxs-lookup"><span data-stu-id="0bd51-104">Creating an Attachment Engine</span></span>

<span data-ttu-id="0bd51-105">附件引擎是處理服務特定設定和分析要求的 DLL。</span><span class="sxs-lookup"><span data-stu-id="0bd51-105">An attachment engine is a DLL that processes service-specific configuration and analysis requests.</span></span> <span data-ttu-id="0bd51-106">換句話說，它會處理標準安全性設定工具集無法處理的處理。</span><span class="sxs-lookup"><span data-stu-id="0bd51-106">In other words, it handles the processing that cannot be handled by the standard Security Configuration tool set.</span></span>

<span data-ttu-id="0bd51-107">若要建立附件引擎，您必須執行下列三個功能：</span><span class="sxs-lookup"><span data-stu-id="0bd51-107">To create an attachment engine, you must implement the following three functions:</span></span>

-   <span data-ttu-id="0bd51-108">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)，它會計算服務設定和儲存在安全性資料庫中設定之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0bd51-108">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="0bd51-109">這些差異會寫入安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="0bd51-109">These differences are written to the security database.</span></span> <span data-ttu-id="0bd51-110">如需詳細資訊，請參閱 [執行 SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd51-110">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>
-   <span data-ttu-id="0bd51-111">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)，會設定嵌入式管理單元使用者介面中指定的服務。</span><span class="sxs-lookup"><span data-stu-id="0bd51-111">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span> <span data-ttu-id="0bd51-112">如需詳細資訊，請參閱 [執行 SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd51-112">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md).</span></span>
-   <span data-ttu-id="0bd51-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)，它會更新安全性資料庫中服務的基本設定和設定分析。</span><span class="sxs-lookup"><span data-stu-id="0bd51-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span> <span data-ttu-id="0bd51-114">如需詳細資訊，請參閱 [執行 SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd51-114">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md).</span></span>

<span data-ttu-id="0bd51-115">安全性設定工具集會實行一組支援函式，讓您的應用程式可以呼叫這些函式，以查詢及設定安全性資料庫中的資訊。</span><span class="sxs-lookup"><span data-stu-id="0bd51-115">The Security Configuration tool set implements a set of support functions that your application can call to query and set information in the security database.</span></span> <span data-ttu-id="0bd51-116">如需詳細資訊，請參閱附加函式 [回呼函數](management-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd51-116">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="0bd51-117">建立附件引擎 DLL 之後，您必須使用「安全性設定」工具組來註冊它。</span><span class="sxs-lookup"><span data-stu-id="0bd51-117">After you create an attachment engine DLL, you must register it with the Security Configuration tool set.</span></span> <span data-ttu-id="0bd51-118">[註冊附件引擎](registering-an-attachment-engine.md)時，會說明此程式。</span><span class="sxs-lookup"><span data-stu-id="0bd51-118">This process is described in [Registering an Attachment Engine](registering-an-attachment-engine.md).</span></span>

<span data-ttu-id="0bd51-119">除了建立附件引擎之外，您還必須建立附件嵌入式管理單元延伸模組。</span><span class="sxs-lookup"><span data-stu-id="0bd51-119">In addition to creating an attachment engine, you must also create an attachment snap-in extension.</span></span> <span data-ttu-id="0bd51-120">嵌入式管理單元擴充功能可提供使用者介面給服務特定的工作。</span><span class="sxs-lookup"><span data-stu-id="0bd51-120">The snap-in extension provides a user interface for service-specific tasks.</span></span> <span data-ttu-id="0bd51-121">當使用者使用嵌入式管理單元擴充功能指定新的設定時，會將要求傳遞至適當的附件引擎。</span><span class="sxs-lookup"><span data-stu-id="0bd51-121">When the user specifies a new configuration using a snap-in extension, the request is passed to the appropriate attachment engine.</span></span> <span data-ttu-id="0bd51-122">然後，引擎會連線到服務並變更其設定。</span><span class="sxs-lookup"><span data-stu-id="0bd51-122">The engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="0bd51-123">如果您未執行嵌入式管理單元延伸模組，使用者將無法變更服務設定或分析。</span><span class="sxs-lookup"><span data-stu-id="0bd51-123">If you do not implement a snap-in extension, users will have no way to change the service configuration or analysis.</span></span> <span data-ttu-id="0bd51-124">如需有關如何建立附件嵌入式管理單元延伸模組的詳細資訊，請參閱 [建立附件嵌入式管理單元延伸](creating-an-attachment-snap-in-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd51-124">For more information on how to create an attachment snap-in extension, see [Creating an Attachment Snap-in Extension](creating-an-attachment-snap-in-extension.md).</span></span>

 

 



