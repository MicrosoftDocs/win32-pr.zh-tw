---
description: COM + 提供簡單的程式設計模型，以使用其自動服務。
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: COM + 服務入門
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317912"
---
# <a name="com-services-primer"></a><span data-ttu-id="346f0-103">COM + 服務入門</span><span class="sxs-lookup"><span data-stu-id="346f0-103">COM+ Services Primer</span></span>

<span data-ttu-id="346f0-104">COM + 提供簡單的程式設計模型，以使用其自動服務。</span><span class="sxs-lookup"><span data-stu-id="346f0-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="346f0-105">您可以直接將這些服務設定為元件及其方法的宣告式屬性。</span><span class="sxs-lookup"><span data-stu-id="346f0-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="346f0-106">當您設定這些屬性時，COM + 會視需要自動將要求的服務傳遞給物件。</span><span class="sxs-lookup"><span data-stu-id="346f0-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="346f0-107">本入門會以三個已定義的步驟逐步解說範例元件程式碼，以顯示 COM + 服務的運作方式。</span><span class="sxs-lookup"><span data-stu-id="346f0-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="346f0-108">這項資訊的複雜度會建立為步驟進度。</span><span class="sxs-lookup"><span data-stu-id="346f0-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="346f0-109">程式碼著重于簡化的程式設計模型，使用交易處理來示範基本的 COM + 原則。</span><span class="sxs-lookup"><span data-stu-id="346f0-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="346f0-110">下列每個步驟說明 COM + 服務的基本層面：</span><span class="sxs-lookup"><span data-stu-id="346f0-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="346f0-111">步驟1：建立交易式元件</span><span class="sxs-lookup"><span data-stu-id="346f0-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="346f0-112">步驟2：跨多個元件擴充交易</span><span class="sxs-lookup"><span data-stu-id="346f0-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="346f0-113">步驟3：重複使用元件</span><span class="sxs-lookup"><span data-stu-id="346f0-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="346f0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="346f0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346f0-115">COM + 程式設計總覽</span><span class="sxs-lookup"><span data-stu-id="346f0-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="346f0-116">COM + 應用程式總覽</span><span class="sxs-lookup"><span data-stu-id="346f0-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="346f0-117">設定 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="346f0-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="346f0-118">COM + 內容和執行緒模型</span><span class="sxs-lookup"><span data-stu-id="346f0-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="346f0-119">建立 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="346f0-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="346f0-120">設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="346f0-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 



