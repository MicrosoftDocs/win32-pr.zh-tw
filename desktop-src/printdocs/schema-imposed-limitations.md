---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed 限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975613"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="87d0c-104">Schema-Imposed 限制</span><span class="sxs-lookup"><span data-stu-id="87d0c-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="87d0c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="87d0c-105">This topic is not current.</span></span> <span data-ttu-id="87d0c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="87d0c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87d0c-107">PrintCapabilities 架構提供 PrintCapabilities 作者大量的彈性和表達，可用於裝置描述。</span><span class="sxs-lookup"><span data-stu-id="87d0c-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="87d0c-108">不過，設定相依性對此彈性和表達有限制。</span><span class="sxs-lookup"><span data-stu-id="87d0c-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="87d0c-109">ParameterDef 實例、功能元素清單、每個功能內的選項實例清單，以及每個選項內的 ScoredProperty 實例都不得包含設定相依性。</span><span class="sxs-lookup"><span data-stu-id="87d0c-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="87d0c-110">PrintCapabilities 檔提供者必須偵測到不正確設定組合，而且必須加以解決。</span><span class="sxs-lookup"><span data-stu-id="87d0c-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87d0c-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="87d0c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d0c-112">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="87d0c-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



