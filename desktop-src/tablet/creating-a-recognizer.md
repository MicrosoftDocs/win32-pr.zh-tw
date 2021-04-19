---
description: 如果您選擇這樣做，則您的應用程式可以提供自己的辨識器執行。 本節說明為您的應用程式建立可搭配 Tablet PC 平臺 API 使用之自訂應用程式辨識器的需求。
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: 建立辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979718"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="3227e-104">建立辨識器</span><span class="sxs-lookup"><span data-stu-id="3227e-104">Creating a Recognizer</span></span>

<span data-ttu-id="3227e-105">如果您選擇這樣做，則您的應用程式可以提供自己的辨識器執行。</span><span class="sxs-lookup"><span data-stu-id="3227e-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="3227e-106">本節說明為您的應用程式建立可搭配 Tablet PC 平臺 API 使用之自訂應用程式辨識器的需求。</span><span class="sxs-lookup"><span data-stu-id="3227e-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="3227e-107">[Tablet PC 輸入面板] 或 [Microsoft Windows 筆記本不會使用自訂應用程式辨識器。</span><span class="sxs-lookup"><span data-stu-id="3227e-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="3227e-108">這些附屬應用程式只會使用已測試過的辨識器。</span><span class="sxs-lookup"><span data-stu-id="3227e-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="3227e-109">下列各節詳細說明自訂辨識器的實作為：</span><span class="sxs-lookup"><span data-stu-id="3227e-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="3227e-110">辨識 API 架構</span><span class="sxs-lookup"><span data-stu-id="3227e-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="3227e-111">[必要的辨識 Api](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3227e-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="3227e-112">HRECOGNIZER 和 HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="3227e-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="3227e-113">辨識器 >lattice 結構</span><span class="sxs-lookup"><span data-stu-id="3227e-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="3227e-114">註冊您的辨識器 DLL</span><span class="sxs-lookup"><span data-stu-id="3227e-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="3227e-115">辨識器執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="3227e-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="3227e-116">一般呼叫順序</span><span class="sxs-lookup"><span data-stu-id="3227e-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="3227e-117">辨識器 DLL 範例範本</span><span class="sxs-lookup"><span data-stu-id="3227e-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="3227e-118">手勢的 Unicode 範圍值</span><span class="sxs-lookup"><span data-stu-id="3227e-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="3227e-119">辨識器 Api</span><span class="sxs-lookup"><span data-stu-id="3227e-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
