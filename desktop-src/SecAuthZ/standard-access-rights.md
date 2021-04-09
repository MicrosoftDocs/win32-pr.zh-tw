---
description: 每一種安全物件類型都有一組存取權限，這些許可權會對應至該物件類型的特定作業。
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: 標準存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848233"
---
# <a name="standard-access-rights"></a><span data-ttu-id="e832b-103">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="e832b-103">Standard Access Rights</span></span>

<span data-ttu-id="e832b-104">每一種安全物件類型都有一組存取權限，這些許可權會對應至該物件類型的特定作業。</span><span class="sxs-lookup"><span data-stu-id="e832b-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="e832b-105">除了這些特定物件的存取權限之外，還提供一組標準存取權限，以對應至大部分型別安全物件的一般作業。</span><span class="sxs-lookup"><span data-stu-id="e832b-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="e832b-106">[存取遮罩格式](access-mask-format.md)包含標準存取權限的一組位。</span><span class="sxs-lookup"><span data-stu-id="e832b-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="e832b-107">下列適用于標準存取權限的 Windows 常數定義于 Winnt. h 中。</span><span class="sxs-lookup"><span data-stu-id="e832b-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="e832b-108">常數</span><span class="sxs-lookup"><span data-stu-id="e832b-108">Constant</span></span>      | <span data-ttu-id="e832b-109">意義</span><span class="sxs-lookup"><span data-stu-id="e832b-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e832b-110">刪除</span><span class="sxs-lookup"><span data-stu-id="e832b-110">DELETE</span></span>        | <span data-ttu-id="e832b-111">刪除物件的權限。</span><span class="sxs-lookup"><span data-stu-id="e832b-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e832b-112">讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="e832b-112">READ\_CONTROL</span></span> | <span data-ttu-id="e832b-113">讀取物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中資訊的許可權，不包括 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 中的資訊 (SACL) 。</span><span class="sxs-lookup"><span data-stu-id="e832b-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="e832b-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="e832b-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="e832b-115">使用同步物件的權限。</span><span class="sxs-lookup"><span data-stu-id="e832b-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="e832b-116">這可讓執行緒等候，直到物件處於已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="e832b-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="e832b-117">某些物件類型不支援此存取權。</span><span class="sxs-lookup"><span data-stu-id="e832b-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="e832b-118">寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="e832b-118">WRITE\_DAC</span></span>    | <span data-ttu-id="e832b-119">在物件的安全描述項中，修改 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 的許可權。</span><span class="sxs-lookup"><span data-stu-id="e832b-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="e832b-120">寫入 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="e832b-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="e832b-121">變更物件安全性描述元中所有人的權限。</span><span class="sxs-lookup"><span data-stu-id="e832b-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="e832b-122">Winnt 也會定義下列標準存取權限常數的組合。</span><span class="sxs-lookup"><span data-stu-id="e832b-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="e832b-123">常數</span><span class="sxs-lookup"><span data-stu-id="e832b-123">Constant</span></span>                   | <span data-ttu-id="e832b-124">意義</span><span class="sxs-lookup"><span data-stu-id="e832b-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e832b-125">標準 \_ 許可權 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="e832b-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="e832b-126">結合了刪除、讀取 \_ 控制、寫入 \_ DAC、寫入 \_ 擁有者和同步存取。</span><span class="sxs-lookup"><span data-stu-id="e832b-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="e832b-127">標準 \_ 許可權 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="e832b-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="e832b-128">目前已定義為相等的讀取 \_ 控制。</span><span class="sxs-lookup"><span data-stu-id="e832b-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="e832b-129">標準 \_ 許可權 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="e832b-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="e832b-130">目前已定義為相等的讀取 \_ 控制。</span><span class="sxs-lookup"><span data-stu-id="e832b-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="e832b-131">\_需要標準許可權 \_</span><span class="sxs-lookup"><span data-stu-id="e832b-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="e832b-132">結合了刪除、讀取 \_ 控制、寫入 \_ DAC，以及寫入 \_ 擁有者存取權。</span><span class="sxs-lookup"><span data-stu-id="e832b-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="e832b-133">標準 \_ 許可權 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="e832b-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="e832b-134">目前已定義為相等的讀取 \_ 控制。</span><span class="sxs-lookup"><span data-stu-id="e832b-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
