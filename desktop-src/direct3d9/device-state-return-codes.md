---
description: 方法和函式的一些可能傳回碼的清單。
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187451"
---
# <a name="s_present"></a><span data-ttu-id="51f70-103">\_存在</span><span class="sxs-lookup"><span data-stu-id="51f70-103">S\_PRESENT</span></span>

<span data-ttu-id="51f70-104">方法和函式的一些可能傳回碼的清單。</span><span class="sxs-lookup"><span data-stu-id="51f70-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f70-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="51f70-105">\#define</span></span>                  | <span data-ttu-id="51f70-106">Description</span><span class="sxs-lookup"><span data-stu-id="51f70-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="51f70-107">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="51f70-107">S\_OK</span></span>                     | <span data-ttu-id="51f70-108">裝置正在正常執行，並可用於轉譯。</span><span class="sxs-lookup"><span data-stu-id="51f70-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51f70-109">\_存在 \_ PIXELS OCCLUDED</span><span class="sxs-lookup"><span data-stu-id="51f70-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="51f70-110">展示區域為 pixels occluded。</span><span class="sxs-lookup"><span data-stu-id="51f70-110">The presentation area is occluded.</span></span> <span data-ttu-id="51f70-111">遮蔽表示展示視窗會最小化，或另一個裝置在與展示視窗相同的監視器上進入全螢幕模式，而展示視窗完全在該監視器上。</span><span class="sxs-lookup"><span data-stu-id="51f70-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="51f70-112">如果另一個視窗涵蓋了工作區，就不會發生遮蔽。</span><span class="sxs-lookup"><span data-stu-id="51f70-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="51f70-113">Pixels occluded 應用程式可以繼續轉譯，而且所有呼叫都將會成功，但不會更新 pixels occluded 呈現視窗。</span><span class="sxs-lookup"><span data-stu-id="51f70-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="51f70-114">最好的情況是，應用程式應該停止使用裝置轉譯至展示視窗，並持續呼叫 [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) ，直到 \_ [確定] 或 [ \_ 存在] \_ 模式變更為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="51f70-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="51f70-115">\_目前的 \_ 模式 \_ 已變更</span><span class="sxs-lookup"><span data-stu-id="51f70-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="51f70-116">桌面顯示模式已變更。</span><span class="sxs-lookup"><span data-stu-id="51f70-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="51f70-117">應用程式可以繼續轉譯，但可能會有色彩轉換/延展。</span><span class="sxs-lookup"><span data-stu-id="51f70-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="51f70-118">挑選類似于目前顯示模式的背景緩衝區格式，然後呼叫 Reset 以重新建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="51f70-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="51f70-119">裝置會在呼叫重設之後離開此狀態。</span><span class="sxs-lookup"><span data-stu-id="51f70-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="51f70-120">其他錯誤碼包含在 [D3DERR](d3derr.md)中。</span><span class="sxs-lookup"><span data-stu-id="51f70-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51f70-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="51f70-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51f70-122">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="51f70-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




