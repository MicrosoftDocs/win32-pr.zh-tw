---
title: Visual Basic 私用介面
description: Visual Basic 私用介面
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022094"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="5d8cb-103">Visual Basic 私用介面</span><span class="sxs-lookup"><span data-stu-id="5d8cb-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="5d8cb-104">在這裡會為元件類別識別 Visual Basic 所執行的兩個介面。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="5d8cb-105">控制項應該不需要這些類別，因為控制項可能會在無法使用時提供替代功能。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="5d8cb-106">[**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat)介面可讓控制項在格式化資料時，更妥善地整合到 Visual Basic 環境中。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="5d8cb-107">CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat</span><span class="sxs-lookup"><span data-stu-id="5d8cb-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="5d8cb-108">[**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)介面允許控制項列舉 VB 表單上的其他控制項。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="5d8cb-109">CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl</span><span class="sxs-lookup"><span data-stu-id="5d8cb-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="5d8cb-110">另外還有兩個額外的私用介面（ [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) 和 [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)），雖然它們並未定義元件類別。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="5d8cb-111">不建議使用這四個介面，因為 Visual Basic 以外的容器不支援這些介面。</span><span class="sxs-lookup"><span data-stu-id="5d8cb-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d8cb-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d8cb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d8cb-113">元件類別</span><span class="sxs-lookup"><span data-stu-id="5d8cb-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




