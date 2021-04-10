---
title: 一個 DLL 中的多個控制項
description: 一個 DLL 中的多個控制項
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020880"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="4c26e-103">一個 DLL 中的多個控制項</span><span class="sxs-lookup"><span data-stu-id="4c26e-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="4c26e-104">單一 .ocx DLL 可以容器化任意數目的 ActiveX 控制項，進而簡化一組相關控制項的散發和使用。</span><span class="sxs-lookup"><span data-stu-id="4c26e-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="4c26e-105">如果您在單一 DLL 中傳送多個控制項，請務必在封裝的每個控制項名稱中包含廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="4c26e-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="4c26e-106">在每個控制項名稱中包含廠商的名稱，可讓使用者輕鬆地識別封裝內的控制項。</span><span class="sxs-lookup"><span data-stu-id="4c26e-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="4c26e-107">例如，如果您送出的 DLL 會執行三個控制項，Con1、Con2 和 Con3，則控制項名稱應該是：</span><span class="sxs-lookup"><span data-stu-id="4c26e-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="4c26e-108">*您的公司名稱* Con1 控制項</span><span class="sxs-lookup"><span data-stu-id="4c26e-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="4c26e-109">*您的公司名稱* Con2 控制項</span><span class="sxs-lookup"><span data-stu-id="4c26e-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="4c26e-110">*您的公司名稱* Con3 控制項</span><span class="sxs-lookup"><span data-stu-id="4c26e-110">*Your company name* Con3 Control</span></span>

 

 




