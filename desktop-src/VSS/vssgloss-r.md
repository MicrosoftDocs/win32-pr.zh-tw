---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: 'R (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970998"
---
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="ee0a7-103">R (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="ee0a7-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ee0a7-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ee0a7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ee0a7-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**請求**</span><span class="sxs-lookup"><span data-stu-id="ee0a7-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="ee0a7-106">與 VSS 互動以建立和管理一或多個磁片區陰影複製和陰影複製集的任何程式，這是最少的。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="ee0a7-107">通常，要求者會管理陰影複製以支援一些其他功能，例如備份和還原作業和磁片鏡像。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="ee0a7-108">另請參閱 [*陰影*](vssgloss-s.md)複製、 [*陰影複製集*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee0a7-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore 方法**</span><span class="sxs-lookup"><span data-stu-id="ee0a7-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="ee0a7-110">Restore process 方法的規格。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-110">A specification of the restore process method.</span></span> <span data-ttu-id="ee0a7-111">它會控制還原時是否覆寫檔案等問題。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="ee0a7-112">如果還原方法設定與還原目標的設定衝突，則會優先使用還原目標。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="ee0a7-113">另請參閱 *還原目標*。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="ee0a7-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**還原目標**</span><span class="sxs-lookup"><span data-stu-id="ee0a7-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="ee0a7-115">在 VSS 下，還原目標是指要求者如何還原檔案的規格，例如，如果它應該覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="ee0a7-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



