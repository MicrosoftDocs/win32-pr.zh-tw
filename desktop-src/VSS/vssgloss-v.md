---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: cbaa7eff-a88b-4b0e-b7b5-5c0d99397942
title: 'V (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da999c820e7a18ce27fc6fac144f88d1d1dafee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511508"
---
# <a name="v-volume-shadow-copy-service"></a><span data-ttu-id="c486c-103">V (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="c486c-103">V (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="c486c-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c486c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c486c-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**體積**</span><span class="sxs-lookup"><span data-stu-id="c486c-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="c486c-106">邏輯儲存體單位。</span><span class="sxs-lookup"><span data-stu-id="c486c-106">A logical storage unit.</span></span> <span data-ttu-id="c486c-107">磁片區是陰影複製建立作業的目標。</span><span class="sxs-lookup"><span data-stu-id="c486c-107">A volume is the target of shadow copy creation operations.</span></span>

</dd> <dt>

<span data-ttu-id="c486c-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**磁片區 GUID 名稱**</span><span class="sxs-lookup"><span data-stu-id="c486c-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**volume GUID name**</span></span>
</dt> <dd>

<span data-ttu-id="c486c-109">磁片區的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="c486c-109">A unique name for a volume.</span></span> <span data-ttu-id="c486c-110">磁片區 GUID 名稱是下列格式的字串：</span><span class="sxs-lookup"><span data-stu-id="c486c-110">A volume GUID name is a string of the following form:</span></span>

<span data-ttu-id="c486c-111">\\\\?\\磁片區 {GUID}</span><span class="sxs-lookup"><span data-stu-id="c486c-111">\\\\?\\Volume{GUID}</span></span>\\

<span data-ttu-id="c486c-112"> (記下尾端的 " \\ " ) 其中 GUID 是磁片區的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c486c-112">(note the trailing "\\") where GUID is a globally unique identifier for the volume.</span></span> <span data-ttu-id="c486c-113">作業系統會在第一次遇到磁片區時指派磁片區名稱，例如在格式化或安裝期間。</span><span class="sxs-lookup"><span data-stu-id="c486c-113">The operating system assigns a volume name when it first encounters a volume, for example, during formatting or installation.</span></span>

<span data-ttu-id="c486c-114">請注意，磁片區可以有一個以上的磁片區 GUID 名稱。</span><span class="sxs-lookup"><span data-stu-id="c486c-114">Note that a volume can have more than one volume GUID name.</span></span>

</dd> </dl>

 

 



