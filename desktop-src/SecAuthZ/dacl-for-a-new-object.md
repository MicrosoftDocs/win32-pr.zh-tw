---
description: 新物件的 DACL
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: 新物件的 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114133"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="6c76a-103">新物件的 DACL</span><span class="sxs-lookup"><span data-stu-id="6c76a-103">DACL for a New Object</span></span>

<span data-ttu-id="6c76a-104">系統會使用下列演算法來建立最新安全物件類型的 DACL：</span><span class="sxs-lookup"><span data-stu-id="6c76a-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="6c76a-105">物件的 DACL 是物件的建立者所指定之 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 中的 dacl。</span><span class="sxs-lookup"><span data-stu-id="6c76a-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="6c76a-106">除非 \_ \_ 已在安全描述項的控制位中設定 SE DACL 保護的位，否則系統會將任何可繼承的 ace 合併至指定的 DACL。</span><span class="sxs-lookup"><span data-stu-id="6c76a-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="6c76a-107">如果建立者未指定安全描述項，系統會從可繼承的 Ace 建立物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="6c76a-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="6c76a-108">如果未指定任何安全描述項，而且沒有可繼承的 Ace，則物件的 DACL 是建立者之 [*主要*](/windows/desktop/SecGloss/p-gly) 或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly) 中的預設 dacl。</span><span class="sxs-lookup"><span data-stu-id="6c76a-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="6c76a-109">如果沒有指定、繼承或預設的 DACL，系統就會建立沒有 DACL 的物件，讓每個人都能完全存取該物件。</span><span class="sxs-lookup"><span data-stu-id="6c76a-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="6c76a-110">系統會使用不同的演算法來建立新 Active Directory 物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="6c76a-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="6c76a-111">如需詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects)。</span><span class="sxs-lookup"><span data-stu-id="6c76a-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
