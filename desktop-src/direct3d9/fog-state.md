---
description: 霧化效果可讓3D 場景更具逼真。
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: " (Direct3D 9) 的霧化狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385497"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="8898f-103"> (Direct3D 9) 的霧化狀態</span><span class="sxs-lookup"><span data-stu-id="8898f-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="8898f-104">霧化效果可讓3D 場景更具逼真。</span><span class="sxs-lookup"><span data-stu-id="8898f-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="8898f-105">您可以使用不超過模擬霧化的霧化效果。</span><span class="sxs-lookup"><span data-stu-id="8898f-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="8898f-106">它們也可以減少具有距離的場景清晰度。</span><span class="sxs-lookup"><span data-stu-id="8898f-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="8898f-107">這會反映真實世界中發生的狀況;當物件從使用者變得更遠時，其詳細資料就比較不相異。</span><span class="sxs-lookup"><span data-stu-id="8898f-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="8898f-108">如需在應用程式中使用霧化的詳細資訊，請參閱 [ (Direct3D 9) 的霧化 ](fog.md)。</span><span class="sxs-lookup"><span data-stu-id="8898f-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="8898f-109">C + + 應用程式會透過裝置呈現狀態控制霧化。</span><span class="sxs-lookup"><span data-stu-id="8898f-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="8898f-110">[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)列舉型別包含的狀態可控制是否使用圖元 (資料表) 或頂點模糊、其色彩、系統套用的霧化公式，以及公式的參數。</span><span class="sxs-lookup"><span data-stu-id="8898f-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="8898f-111">您可以藉由將 D3DRS \_ FOGENABLE 轉譯狀態設為 **TRUE** 來啟用霧化。</span><span class="sxs-lookup"><span data-stu-id="8898f-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="8898f-112">您可以使用 D3DRS FOGCOLOR 轉譯狀態將霧化色彩設定為任何色彩值 \_ ; 會忽略霧化色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="8898f-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="8898f-113">D3DRS \_ FOGTABLEMODE 和 D3DRS \_ FOGVERTEXMODE 轉譯狀態會控制適用于霧化計算的霧化公式，並間接控制要套用的霧化類型。</span><span class="sxs-lookup"><span data-stu-id="8898f-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="8898f-114">這兩種轉譯狀態都可以設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="8898f-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="8898f-115">將 [轉譯狀態] 設定為 D3DFOG [無] 會 \_ 分別停用圖元或頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="8898f-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="8898f-116">如果這兩種轉譯狀態都設為有效的模式，則系統只會套用圖元霧化效果。</span><span class="sxs-lookup"><span data-stu-id="8898f-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="8898f-117">D3DRS \_ FOGSTART 和 D3DRS \_ FOGEND 轉譯狀態會控制 D3DFOG 線性模式的霧化公式參數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8898f-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="8898f-118">D3DRS \_ FOGDENSITY 轉譯狀態會控制指數霧化模式中的霧化密度。</span><span class="sxs-lookup"><span data-stu-id="8898f-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="8898f-119">如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="8898f-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8898f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="8898f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8898f-121">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="8898f-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
