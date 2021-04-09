---
description: '複製和共用 (Direct3D 9) '
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: '複製和共用 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847547"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="a98e8-103">複製和共用 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a98e8-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="a98e8-104">複製參數</span><span class="sxs-lookup"><span data-stu-id="a98e8-104">Cloning Parameters</span></span>

<span data-ttu-id="a98e8-105">複製有下列限制。</span><span class="sxs-lookup"><span data-stu-id="a98e8-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="a98e8-106">複製會繼承原始效果的集區。</span><span class="sxs-lookup"><span data-stu-id="a98e8-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="a98e8-107">請參閱共用參數一節。</span><span class="sxs-lookup"><span data-stu-id="a98e8-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="a98e8-108">複製會繼承原始效果的技術、傳遞、參數和注釋 (包括以 [**ID3DXEffect**](id3dxeffect.md)) 新增的所有批註。</span><span class="sxs-lookup"><span data-stu-id="a98e8-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="a98e8-109">複製會繼承原始效果動態加入的注釋。</span><span class="sxs-lookup"><span data-stu-id="a98e8-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="a98e8-110">如果原始效果的集區不是 **Null** ，而且原始效果包含共用裝置相依參數 (例如紋理或著色器) ，則複製到新裝置上的作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a98e8-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="a98e8-111">共用參數</span><span class="sxs-lookup"><span data-stu-id="a98e8-111">Sharing Parameters</span></span>

<span data-ttu-id="a98e8-112">集區是在不同效果之間共用效果參數的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a98e8-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="a98e8-113">若要將參數新增至集區，請在建立效果時指定共用的使用方式。</span><span class="sxs-lookup"><span data-stu-id="a98e8-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="a98e8-114">集區具有下列限制。</span><span class="sxs-lookup"><span data-stu-id="a98e8-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="a98e8-115">第一次將包含該 (共用) 參數的效果新增至集區時，會將參數新增至集區。</span><span class="sxs-lookup"><span data-stu-id="a98e8-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="a98e8-116">集區會從第一個共用參數取得初始值;之後共用的參數會從集區中取得其值。</span><span class="sxs-lookup"><span data-stu-id="a98e8-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="a98e8-117">當共用參數的所有效果參考都釋出時，就會從集區刪除參數。</span><span class="sxs-lookup"><span data-stu-id="a98e8-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="a98e8-118">集區中包含相同 (共用) 裝置相依參數的所有效果都必須有相同的裝置。</span><span class="sxs-lookup"><span data-stu-id="a98e8-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="a98e8-119">**Null** 可以用來指定沒有集區，在此情況下不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="a98e8-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="a98e8-120">這幾乎相當於僅針對此效果指定唯一的集區。</span><span class="sxs-lookup"><span data-stu-id="a98e8-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="a98e8-121">唯一的差異在於複製效果時，複製不會與原始的共用參數共用。</span><span class="sxs-lookup"><span data-stu-id="a98e8-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a98e8-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="a98e8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a98e8-123">效果格式</span><span class="sxs-lookup"><span data-stu-id="a98e8-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



