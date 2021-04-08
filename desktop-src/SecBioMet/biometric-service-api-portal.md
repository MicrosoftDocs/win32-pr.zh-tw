---
title: Windows 生物特徵辨識架構
description: 您可以使用 Windows 生物特徵辨識架構 API 來建立用戶端應用程式，以安全地捕捉、儲存和比較使用者生物特徵辨識資訊。
ms.assetid: d9ac9ec1-bb34-402d-a590-73d5070b97ba
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API，首頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4341f09f3141e1be77bcdf0987ee1273ffddcf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675160"
---
# <a name="windows-biometric-framework"></a><span data-ttu-id="d4476-105">Windows 生物特徵辨識架構</span><span class="sxs-lookup"><span data-stu-id="d4476-105">Windows Biometric Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="d4476-106">目的</span><span class="sxs-lookup"><span data-stu-id="d4476-106">Purpose</span></span>

<span data-ttu-id="d4476-107">您可以使用 Windows 生物特徵辨識架構 API 來建立用戶端應用程式，以安全地捕捉、儲存和比較使用者生物特徵辨識資訊。</span><span class="sxs-lookup"><span data-stu-id="d4476-107">You can use the Windows Biometric Framework API to create client applications that securely capture, save, and compare end-user biometric information.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d4476-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="d4476-108">Developer audience</span></span>

<span data-ttu-id="d4476-109">使用此 API 的開發人員應該熟悉 C 和 c + + 程式設計語言和 Windows 型程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="d4476-109">Developers who use this API should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d4476-110">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="d4476-110">Run-time requirements</span></span>

<span data-ttu-id="d4476-111">從 Windows Server 2008 R2 和 Windows 7 開始支援 Windows 生物特徵辨識架構 API。</span><span class="sxs-lookup"><span data-stu-id="d4476-111">The Windows Biometric Framework API is supported beginning with Windows Server 2008 R2 and Windows 7.</span></span> <span data-ttu-id="d4476-112">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="d4476-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4476-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="d4476-113">In this section</span></span>



| <span data-ttu-id="d4476-114">主題</span><span class="sxs-lookup"><span data-stu-id="d4476-114">Topic</span></span>                                                                                       | <span data-ttu-id="d4476-115">描述</span><span class="sxs-lookup"><span data-stu-id="d4476-115">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4476-116">生物特徵辨識架構總覽</span><span class="sxs-lookup"><span data-stu-id="d4476-116">Biometric Framework overview</span></span>](biometric-framework-overview.md)<br/>                 | <span data-ttu-id="d4476-117">描述 Windows 中生物特徵辨識的原生支援。</span><span class="sxs-lookup"><span data-stu-id="d4476-117">Describes the native support for biometrics in Windows.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d4476-118">建立用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="d4476-118">Creating client applications</span></span>](creating-client-applications.md)<br/>                 | <span data-ttu-id="d4476-119">您可以使用用戶端 API，在您的應用程式中捕獲並使用生物特徵辨識資訊。</span><span class="sxs-lookup"><span data-stu-id="d4476-119">You can use the client API to capture and use biometric information in your applications.</span></span><br/>                                                     |
| [<span data-ttu-id="d4476-120">建立介面卡外掛程式</span><span class="sxs-lookup"><span data-stu-id="d4476-120">Creating Adapter Plug-ins</span></span>](creating-adapter-plug-ins.md)<br/>                       | <span data-ttu-id="d4476-121">您可以使用本節中的主題來建立引擎介面卡、感應器介面卡和存放裝置介面卡。</span><span class="sxs-lookup"><span data-stu-id="d4476-121">You can create engine adapters, sensor adapters, and storage adapters using the topics in this section.</span></span><br/>                                       |
| [<span data-ttu-id="d4476-122">建立私人感應器集區</span><span class="sxs-lookup"><span data-stu-id="d4476-122">Creating a Private Sensor Pool</span></span>](creating-a-private-sensor-pool.md)<br/>             | <span data-ttu-id="d4476-123">感應器集區有兩種類型：私用和系統。</span><span class="sxs-lookup"><span data-stu-id="d4476-123">There are two types of sensor pools: private and system.</span></span> <span data-ttu-id="d4476-124">本節將說明每一個，並說明如何建立私人感應器集區。</span><span class="sxs-lookup"><span data-stu-id="d4476-124">This section describes each and explains how to create a private sensor pool.</span></span> <br/>       |
| [<span data-ttu-id="d4476-125">Windows 生物特徵辨識架構 API 參考</span><span class="sxs-lookup"><span data-stu-id="d4476-125">Windows Biometric Framework API Reference</span></span>](biometric-service-api-reference.md)<br/> | <span data-ttu-id="d4476-126">可以用來建立用戶端應用程式和外掛程式的函式、結構和其他程式設計專案的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="d4476-126">Detailed descriptions of functions, structures, and other programming elements that can be used to create a client applications and plug-ins.</span></span><br/> |



 

 

 





