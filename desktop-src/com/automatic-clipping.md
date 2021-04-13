---
title: 自動裁剪
description: 自動裁剪
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301515"
---
# <a name="automatic-clipping"></a><span data-ttu-id="017c8-103">自動裁剪</span><span class="sxs-lookup"><span data-stu-id="017c8-103">Automatic Clipping</span></span>

<span data-ttu-id="017c8-104">強烈建議 ActiveX 控制項容器支援自動裁剪其控制項。</span><span class="sxs-lookup"><span data-stu-id="017c8-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="017c8-105">這會讓大部分的控制項更有效率地運作。</span><span class="sxs-lookup"><span data-stu-id="017c8-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="017c8-106">如果支援自動裁剪，則必須支援 AutoClip 環境屬性，並將值 **設為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="017c8-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="017c8-107">自動裁剪是容器的功能，可確保控制項的繪製輸出只會傳送至容器目前的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="017c8-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="017c8-108">在支援自動裁剪的容器中，控制項可以繪製，而不考慮其裁剪區域，因為容器會自動剪下在控制項區域以外發生的任何繪製。</span><span class="sxs-lookup"><span data-stu-id="017c8-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="017c8-109">如果容器不支援自動裁剪，則 CDK 產生的控制項將會在傳遞非 null 裁剪區域時建立額外的父視窗。</span><span class="sxs-lookup"><span data-stu-id="017c8-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="017c8-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="017c8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="017c8-111">容器</span><span class="sxs-lookup"><span data-stu-id="017c8-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




