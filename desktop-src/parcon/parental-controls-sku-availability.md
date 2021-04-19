---
description: 家長監護 SKU 可用性
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: 家長監護 SKU 可用性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981554"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="5888a-103">家長監護 SKU 可用性</span><span class="sxs-lookup"><span data-stu-id="5888a-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="5888a-104">本章節中所述的「家長監護」、「功能」和「Api」目前計畫僅適用于以取用者為焦點的 Sku，例如：</span><span class="sxs-lookup"><span data-stu-id="5888a-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="5888a-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="5888a-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="5888a-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="5888a-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="5888a-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="5888a-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="5888a-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="5888a-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="5888a-109">家長監護只會安裝在這些 Sku 上。</span><span class="sxs-lookup"><span data-stu-id="5888a-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="5888a-110">需要部署至商務 Sku 的解決方案必須：</span><span class="sxs-lookup"><span data-stu-id="5888a-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="5888a-111">偵測並不供應商務 Sku 的家長監護功能。</span><span class="sxs-lookup"><span data-stu-id="5888a-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="5888a-112">偵測並提供設定、記錄和限制的替代方法。</span><span class="sxs-lookup"><span data-stu-id="5888a-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="5888a-113">建議解決方案透過檢查合規性 API 上的 COM CoCreateInstance 是否成功，來偵測家長監護基礎結構的可用性。</span><span class="sxs-lookup"><span data-stu-id="5888a-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="5888a-114">以 Windows Vista 基礎結構為依據的可感知應用程式，也可能想要在支援的 SKU 上隱藏家長監護的 UI 時，隱藏任何自己的 UI 公開設定或其他功能。</span><span class="sxs-lookup"><span data-stu-id="5888a-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="5888a-115">為可見度判斷提供的函式，涵蓋已加入網域的隱藏專案。</span><span class="sxs-lookup"><span data-stu-id="5888a-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



