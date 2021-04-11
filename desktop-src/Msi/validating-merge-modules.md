---
description: 作者應該先針對每個新的或新修改的合併模組執行驗證，再嘗試將模組第一次合併到安裝資料庫中。
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: 驗證合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113825"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="13117-103">驗證合併模組</span><span class="sxs-lookup"><span data-stu-id="13117-103">Validating Merge Modules</span></span>

<span data-ttu-id="13117-104">作者應該先針對每個新的或新修改的合併模組執行驗證，再嘗試將模組第一次合併到安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="13117-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="13117-105">合併模組驗證的運作方式與 [封裝驗證](package-validation.md) 相同，但會使用不同的 [內部一致性評估](internal-consistency-evaluators-ices.md) 工具集， (適用于合併模組的特定) 。</span><span class="sxs-lookup"><span data-stu-id="13117-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="13117-106">如需有關這些 merge module 的詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="13117-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="13117-107">Merge module 會儲存在 merge module 的 .cub 檔中，Mergemod。</span><span class="sxs-lookup"><span data-stu-id="13117-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="13117-108">安裝 Orca 工具或 msival2 時，也會提供標誌 .cub、Darice 和 Mergemod。</span><span class="sxs-lookup"><span data-stu-id="13117-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="13117-109">如需詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="13117-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



