---
description: 附件引擎是處理服務特定設定和分析要求的 DLL。
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: 附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850847"
---
# <a name="attachment-engines"></a><span data-ttu-id="30fab-103">附件引擎</span><span class="sxs-lookup"><span data-stu-id="30fab-103">Attachment Engines</span></span>

<span data-ttu-id="30fab-104">附件引擎是處理服務特定設定和分析要求的 DLL。</span><span class="sxs-lookup"><span data-stu-id="30fab-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="30fab-105">使用者使用附件嵌入式管理單元擴充功能，進行服務專屬的設定和分析要求。</span><span class="sxs-lookup"><span data-stu-id="30fab-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="30fab-106">然後，此要求會透過「安全性設定」嵌入式管理單元傳遞至一般安全性設定引擎，然後將服務特定的處理傳遞至適當的附件引擎。</span><span class="sxs-lookup"><span data-stu-id="30fab-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="30fab-107">附件引擎接著會連接到服務並變更其設定。</span><span class="sxs-lookup"><span data-stu-id="30fab-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="30fab-108">換句話說，附件引擎會提供支援附件嵌入式管理單元擴充功能的後端處理。</span><span class="sxs-lookup"><span data-stu-id="30fab-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="30fab-109">附件引擎必須執行下列三個功能：</span><span class="sxs-lookup"><span data-stu-id="30fab-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="30fab-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)，它會計算服務設定和儲存在安全性資料庫中設定之間的差異。</span><span class="sxs-lookup"><span data-stu-id="30fab-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="30fab-111">這些差異會寫入安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="30fab-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="30fab-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)，會設定嵌入式管理單元使用者介面中指定的服務。</span><span class="sxs-lookup"><span data-stu-id="30fab-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="30fab-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)，它會更新安全性資料庫中服務的基本設定和設定分析。</span><span class="sxs-lookup"><span data-stu-id="30fab-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="30fab-114">為了簡化上述函式的執行，安全性設定工具集會提供支援函式和結構，讓您的應用程式可用來查詢及設定安全性資料庫中的資訊。</span><span class="sxs-lookup"><span data-stu-id="30fab-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="30fab-115">如需詳細資訊，請參閱附加函式 [回呼函數](management-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="30fab-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="30fab-116">當您建立附件引擎 DLL 時，您必須先安裝它，然後再向安全性設定引擎註冊。</span><span class="sxs-lookup"><span data-stu-id="30fab-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="30fab-117">若要註冊 DLL，您可以將特定的金鑰新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="30fab-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="30fab-118">當安全性設定引擎啟動時，它會檢查登錄並載入所有已註冊的附件引擎 Dll。</span><span class="sxs-lookup"><span data-stu-id="30fab-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="30fab-119">然後，它會將服務特定的設定和分析要求傳遞至適當的附件引擎。</span><span class="sxs-lookup"><span data-stu-id="30fab-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="30fab-120">標準設定和分析要求（非服務特定的要求）是由安全性設定引擎處理。</span><span class="sxs-lookup"><span data-stu-id="30fab-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 



