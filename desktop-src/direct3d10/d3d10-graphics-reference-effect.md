---
description: Direct3D API 定義了數個 API 元素，可協助您建立和管理效果系統。
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: " (Direct3D 10 圖形) 的效果參考"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936258"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="ff863-103"> (Direct3D 10 圖形) 的效果參考</span><span class="sxs-lookup"><span data-stu-id="ff863-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="ff863-104">Direct3D API 定義了數個 API 元素，可協助您建立和管理效果系統。</span><span class="sxs-lookup"><span data-stu-id="ff863-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="ff863-105">介面</span><span class="sxs-lookup"><span data-stu-id="ff863-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="ff863-106">函數</span><span class="sxs-lookup"><span data-stu-id="ff863-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="ff863-107">結構</span><span class="sxs-lookup"><span data-stu-id="ff863-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="ff863-108">常數</span><span class="sxs-lookup"><span data-stu-id="ff863-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="ff863-109">效果系統會將狀態指派封裝在效果中。</span><span class="sxs-lookup"><span data-stu-id="ff863-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="ff863-110">每個效果都是管線狀態的集合，可使用狀態欄塊、資源和著色器細分為狀態指派。</span><span class="sxs-lookup"><span data-stu-id="ff863-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="ff863-111">根據效果的大小，您可以選擇在 ASCII 文字字串或效果檔案中執行一個（ ( fx) 。</span><span class="sxs-lookup"><span data-stu-id="ff863-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="ff863-112">若要在效果中組織資訊，請參閱 [效果格式](d3d10-effect-format.md)。</span><span class="sxs-lookup"><span data-stu-id="ff863-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="ff863-113">設計好效果之後，請使用效果 API 在轉譯期間設定裝置中的狀態。</span><span class="sxs-lookup"><span data-stu-id="ff863-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="ff863-114">同樣地，效果系統還支援一系列的反映 API 來取得和設定效果資料。</span><span class="sxs-lookup"><span data-stu-id="ff863-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="ff863-115">如需詳細資訊，請參閱 [效果系統介面 (Direct3D 10) ](d3d10-graphics-programming-guide-effects-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="ff863-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff863-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff863-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff863-117">Direct3D 參考</span><span class="sxs-lookup"><span data-stu-id="ff863-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



