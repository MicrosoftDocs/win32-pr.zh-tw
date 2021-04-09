---
description: 物件 ACL 可以包含它從其父容器繼承的 Ace。
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: ACE 繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943980"
---
# <a name="ace-inheritance"></a><span data-ttu-id="048ed-103">ACE 繼承</span><span class="sxs-lookup"><span data-stu-id="048ed-103">ACE Inheritance</span></span>

<span data-ttu-id="048ed-104">物件的 ACL 可以包含繼承自其父容器的 Ace。</span><span class="sxs-lookup"><span data-stu-id="048ed-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="048ed-105">例如，登錄子機碼可以從登錄階層中其上方的金鑰繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="048ed-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="048ed-106">同樣地，NTFS 檔案系統中的檔案可以從包含它的目錄繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="048ed-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="048ed-107">ACE 的 [**ace \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header) 結構包含一組繼承旗標，這些旗標可控制 ace 繼承以及它附加之物件上的 ace 效果。</span><span class="sxs-lookup"><span data-stu-id="048ed-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="048ed-108">系統會根據 [ACE 繼承的規則](ace-inheritance-rules.md)，來解讀繼承旗標和其他繼承資訊。</span><span class="sxs-lookup"><span data-stu-id="048ed-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="048ed-109">下列功能已增強這些規則：</span><span class="sxs-lookup"><span data-stu-id="048ed-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="048ed-110">支援可 [繼承 ace 的自動傳播](automatic-propagation-of-inheritable-aces.md)。</span><span class="sxs-lookup"><span data-stu-id="048ed-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="048ed-111">區分直接套用至物件之繼承 Ace 和 Ace 的旗標。</span><span class="sxs-lookup"><span data-stu-id="048ed-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="048ed-112">物件特定的 Ace，可讓您指定可繼承 ACE 的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="048ed-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="048ed-113">藉由在 \_ \_ \_ \_ [*安全描述項的*](/windows/desktop/SecGloss/s-gly) 控制位（系統 \_ 資源 \_ 屬性 \_ ACE 和系統 \_ 範圍 \_ 原則 \_ 識別碼 \_ ACE 除外）中設定 se DACL protected 或 se 受保護的位，來防止 DACL 或 SACL 繼承 ace。</span><span class="sxs-lookup"><span data-stu-id="048ed-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
