---
title: 外掛程式參考
description: 介面卡函式、包裝函式，以及用來建立三種類型引擎、感應器和儲存體之自訂外掛程式介面卡的結構。
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API、外掛程式參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462437"
---
# <a name="plug-in-reference"></a><span data-ttu-id="a6d1a-104">外掛程式參考</span><span class="sxs-lookup"><span data-stu-id="a6d1a-104">Plug-in Reference</span></span>

<span data-ttu-id="a6d1a-105">生物識別單元會以各種不同的類型和設定制造。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="a6d1a-106">Windows 生物特徵辨識架構併入可延伸的架構，可讓您藉由建立自訂外掛程式來處理這類各種不同的架構。此架構的核心是稱為生物特徵辨識單位的軟體物件。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="a6d1a-107">您可以將生物識別單位視為抽象概念，以代表架構的生物特徵辨識裝置。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="a6d1a-108">稱為介面卡的外掛程式軟體元件會將生物識別單位連接到相關聯的硬體。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="a6d1a-109">您可以建立三種類型的介面卡。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="a6d1a-110">引擎介面卡會從已捕捉的範例產生生物特徵辨識範本、比對現有範本的範例和索引範本。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="a6d1a-111">感應器介面卡會包裝生物特徵辨識裝置，並提供標準介面來設定感應器、捕獲範例，以及控制生物特徵辨識資料流程向處理引擎的流程。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="a6d1a-112">儲存體介面卡會管理範本資料庫。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a6d1a-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="a6d1a-113">In this section</span></span>



| <span data-ttu-id="a6d1a-114">主題</span><span class="sxs-lookup"><span data-stu-id="a6d1a-114">Topic</span></span>                                                                 | <span data-ttu-id="a6d1a-115">描述</span><span class="sxs-lookup"><span data-stu-id="a6d1a-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6d1a-116">外掛程式函數</span><span class="sxs-lookup"><span data-stu-id="a6d1a-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="a6d1a-117">您可以用來建立組成生物識別單位之介面卡外掛程式的函式。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="a6d1a-118">外掛程式結構</span><span class="sxs-lookup"><span data-stu-id="a6d1a-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="a6d1a-119">Windows 生物特徵辨識架構 API 開發用戶端應用程式的結構。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="a6d1a-120">外掛程式包裝函數</span><span class="sxs-lookup"><span data-stu-id="a6d1a-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="a6d1a-121">包裝函式，可讓您在任何附加至管線的介面卡上呼叫公用函式，而不需要手動取得介面卡的指標。</span><span class="sxs-lookup"><span data-stu-id="a6d1a-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





