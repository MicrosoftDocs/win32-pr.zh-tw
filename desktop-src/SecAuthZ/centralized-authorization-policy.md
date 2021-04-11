---
description: 動態存取控制 (DAC) 案例可針對企業檔案伺服器案例啟用集中式存取控制管理。
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: 集中式授權原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945496"
---
# <a name="centralized-authorization-policy"></a><span data-ttu-id="a5992-103">集中式授權原則</span><span class="sxs-lookup"><span data-stu-id="a5992-103">Centralized Authorization Policy</span></span>

<span data-ttu-id="a5992-104">[動態存取控制 (DAC) 案例](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)可針對企業檔案伺服器案例啟用集中式存取控制管理。</span><span class="sxs-lookup"><span data-stu-id="a5992-104">The [Dynamic Access Control (DAC) scenario](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) enables centralized access control administration for enterprise file server scenarios.</span></span> <span data-ttu-id="a5992-105">大部分的組織都有多個區域，他們想要控制存取權。</span><span class="sxs-lookup"><span data-stu-id="a5992-105">Most organizations have multiple areas in which they want to control access.</span></span>

<span data-ttu-id="a5992-106">範例包括：</span><span class="sxs-lookup"><span data-stu-id="a5992-106">Examples are:</span></span>

-   <span data-ttu-id="a5992-107">控制機密資訊的存取，其中標示為機密的檔案會有特定許可權</span><span class="sxs-lookup"><span data-stu-id="a5992-107">Controlling access to sensitive information, in which files marked as sensitive would have specific permissions</span></span>
-   <span data-ttu-id="a5992-108">控制存取包含個人識別資訊的檔案 (PII. ) </span><span class="sxs-lookup"><span data-stu-id="a5992-108">Controlling access to files containing personally identifiable information (PII.)</span></span>
-   <span data-ttu-id="a5992-109">根據組織的保留原則來限制對檔的存取。</span><span class="sxs-lookup"><span data-stu-id="a5992-109">Limiting access to documents based on the organizations retention policies.</span></span>

<span data-ttu-id="a5992-110">提供數個新的授權原則抽象概念，可讓系統管理員集中定義這些原則，並允許個別定義和維護每個存取需求，但套用為一個原則，以簡化定義流程。</span><span class="sxs-lookup"><span data-stu-id="a5992-110">Several new authorization policy abstractions are provided to allow an administrator to define these policies centrally and to simplify the definition process by allowing each of these access requirements to be defined and maintained separately but applied as one policy.</span></span>

<span data-ttu-id="a5992-111">有兩個新的 Active Directory 原則物件： [集中授權原則](central-authorization-policies.md) (cap) 和 [集中授權原則規則](central-authorization-policy-rule.md) (capr) 是在 windows 8 中引進，可根據宣告和資源屬性的運算式來定義及套用集中式授權原則。</span><span class="sxs-lookup"><span data-stu-id="a5992-111">Two new Active Directory policy objects, a [central authorization policy](central-authorization-policies.md) (cap) and a [central authorization policy rule](central-authorization-policy-rule.md) (capr) are introduced in windows 8 to define and apply centralized authorization policies based on expressions of claims and resource attributes.</span></span> <span data-ttu-id="a5992-112">在使用這些物件時，系統管理員會將 capr 定義為特定的授權原則，以套用至具有特定屬性或符合特定適用性條件的資源。</span><span class="sxs-lookup"><span data-stu-id="a5992-112">in using these objects an administrator defines a capr as a specific authorization policy that can be applied to resources that have a certain attribute or satisfy a certain applicability condition.</span></span> <span data-ttu-id="a5992-113">例如，標示為「高度業務衝擊」的檔。</span><span class="sxs-lookup"><span data-stu-id="a5992-113">for example documents labeled as "high business impact".</span></span> <span data-ttu-id="a5992-114">您可以針對可以表示的組織中每個所需的存取控制原則來定義 capes，而且可以識別其應套用的資源（就 windows 8 dac 運算式而言）。</span><span class="sxs-lookup"><span data-stu-id="a5992-114">capes may be defined for each desired access control policy in an organization that can be expressed, and the resources to which it should be applied can be identified, in terms of windows 8 dac expressions.</span></span> <span data-ttu-id="a5992-115">端點是可在資源上一起套用的 caprs 集合。</span><span class="sxs-lookup"><span data-stu-id="a5992-115">a cap is collection of caprs that can be applied together on resources.</span></span> <span data-ttu-id="a5992-116">下圖顯示帽和維德角的關聯性，以及在定義和套用這些物件至檔案資源時所牽涉到的概念步驟。</span><span class="sxs-lookup"><span data-stu-id="a5992-116">the following diagram shows the relationships of the cap and cape, and the conceptual steps involved in defining and applying these objects to file resources.</span></span> <span data-ttu-id="a5992-117">![capes 和 cap 的關聯性](images/cap.png)</span><span class="sxs-lookup"><span data-stu-id="a5992-117">![relationship of capes and caps](images/cap.png)</span></span>

 

 
