---
description: 所有安全物件都會使用下圖所示的存取遮罩格式來排列其存取權限。
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: 存取遮罩格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849888"
---
# <a name="access-mask-format"></a><span data-ttu-id="897e2-103">存取遮罩格式</span><span class="sxs-lookup"><span data-stu-id="897e2-103">Access Mask Format</span></span>

<span data-ttu-id="897e2-104">所有安全物件都會使用下圖所示的 [*存取遮罩*](/windows/desktop/SecGloss/a-gly) 格式來排列其存取權限。</span><span class="sxs-lookup"><span data-stu-id="897e2-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![存取遮罩格式](images/accctrl4.png)

<span data-ttu-id="897e2-106">以這種格式來說，低序位16位適用于特定物件的存取權限，下8個位適用于 [標準存取權限](standard-access-rights.md)，適用于大部分的物件類型，而4個高序位位可用來指定 [泛型存取權限](generic-access-rights.md) ，每個物件類型都可對應至一組標準和物件特定的許可權。</span><span class="sxs-lookup"><span data-stu-id="897e2-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="897e2-107">存取 \_ 系統 \_ 安全位會對應至 [存取物件之 SACL](sacl-access-right.md)的許可權。</span><span class="sxs-lookup"><span data-stu-id="897e2-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
