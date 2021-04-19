---
description: 新物件的 SACL
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: 新物件的 SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973880"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="3331e-103">新物件的 SACL</span><span class="sxs-lookup"><span data-stu-id="3331e-103">SACL for a New Object</span></span>

<span data-ttu-id="3331e-104">系統會使用下列演算法，為大部分的新安全物件類型建立 SACL：</span><span class="sxs-lookup"><span data-stu-id="3331e-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="3331e-105">物件的 SACL 是物件的建立者所指定之 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 中的 sacl。</span><span class="sxs-lookup"><span data-stu-id="3331e-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="3331e-106">除非 \_ \_ 已在安全描述項的控制位中設定 SE SACL 保護的位，否則系統會將任何可繼承的 ace 合併為指定的 SACL。</span><span class="sxs-lookup"><span data-stu-id="3331e-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="3331e-107">\_ \_ \_ \_ \_ \_ \_ 即使 \_ 已設定 SE SACL 保護的位，父物件的系統資源屬性 ace 和系統範圍原則識別碼 ace 也會合並到新的物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3331e-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="3331e-108">如果建立者未指定安全描述項，系統會從可繼承的 Ace 建立物件的 SACL。</span><span class="sxs-lookup"><span data-stu-id="3331e-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="3331e-109">如果沒有指定或繼承的 SACL，物件就不會有 SACL。</span><span class="sxs-lookup"><span data-stu-id="3331e-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="3331e-110">若要為新物件指定 SACL，物件的建立者必須啟用「SE \_ 安全性 \_ 名稱」 [許可權](privileges.md) 。</span><span class="sxs-lookup"><span data-stu-id="3331e-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="3331e-111">如果新物件的指定 SACL 只包含系統 \_ 資源 \_ 屬性 \_ ace，則不需要「SE \_ 安全性 \_ 名稱」許可權。</span><span class="sxs-lookup"><span data-stu-id="3331e-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="3331e-112">如果物件的 SACL 是從繼承的 Ace 建立的，則建立者不需要此許可權。</span><span class="sxs-lookup"><span data-stu-id="3331e-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="3331e-113">系統會使用不同的演算法來建立新 Active Directory 物件的 SACL。</span><span class="sxs-lookup"><span data-stu-id="3331e-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="3331e-114">如需詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects)。</span><span class="sxs-lookup"><span data-stu-id="3331e-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
