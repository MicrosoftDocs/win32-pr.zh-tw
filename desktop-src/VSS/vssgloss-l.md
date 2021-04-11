---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: 'L (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191362"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="56518-103">L (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="56518-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="56518-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="56518-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="56518-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**邏輯路徑**</span><span class="sxs-lookup"><span data-stu-id="56518-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="56518-106">描述寫入器元件的機制。</span><span class="sxs-lookup"><span data-stu-id="56518-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="56518-107">它是用來表示元件之間的關聯性，尤其是其階層。</span><span class="sxs-lookup"><span data-stu-id="56518-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="56518-108">比方說，如果寫入器管理了數個電子書，它可能會將 " \\ 電子書 \\ book1" 和 " \\ 電子書 book2" 的邏輯路徑指派 \\ 給包含每本書的檔案群組元件。</span><span class="sxs-lookup"><span data-stu-id="56518-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="56518-109">指定子元件時，需要邏輯路徑。</span><span class="sxs-lookup"><span data-stu-id="56518-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="56518-110">依照慣例，會使用反斜線 " \\ " 來分隔邏輯路徑的元素。</span><span class="sxs-lookup"><span data-stu-id="56518-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="56518-111">除此之外，非 **Null** 邏輯路徑中可能會出現的字元沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="56518-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="56518-112">邏輯路徑可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="56518-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="56518-113">依照慣例，具有 **Null** 邏輯路徑的元件會被視為是寫入器邏輯路徑階層的最上層。</span><span class="sxs-lookup"><span data-stu-id="56518-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="56518-114">另請參閱元件和 [*子*](vssgloss-s.md)[*元件*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="56518-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



