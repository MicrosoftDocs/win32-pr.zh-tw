---
title: '常見的錯誤 (AD DS) '
description: 下表包含的常見錯誤清單，可能會根據所要嵌套之群組的範圍而發生。
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- 常見的錯誤廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "104462676"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="a1411-104">常見的錯誤 (AD DS) </span><span class="sxs-lookup"><span data-stu-id="a1411-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="a1411-105">下表包含的常見錯誤清單，可能會根據所要嵌套之群組的範圍而發生。</span><span class="sxs-lookup"><span data-stu-id="a1411-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1411-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a1411-106">HRESULT</span></span></th>
<th><span data-ttu-id="a1411-107">Description</span><span class="sxs-lookup"><span data-stu-id="a1411-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1411-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="a1411-108">0x8007001F</span></span></td>
<td><span data-ttu-id="a1411-109">一般失敗。</span><span class="sxs-lookup"><span data-stu-id="a1411-109">General failure.</span></span> <span data-ttu-id="a1411-110">如果您嘗試進行下列動作，就會發生此錯誤：</span><span class="sxs-lookup"><span data-stu-id="a1411-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="a1411-111">將網域本機群組新增至全域或萬用群組或另一個網域中的網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="a1411-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="a1411-112">您只能將網域本機群組新增為相同網域中其他網域本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="a1411-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="a1411-113">將萬用群組新增至全域群組。</span><span class="sxs-lookup"><span data-stu-id="a1411-113">Add a universal group to a global group.</span></span> <span data-ttu-id="a1411-114">萬用群組可以新增至通用和網網域本機群組，但不能新增至全域群組。</span><span class="sxs-lookup"><span data-stu-id="a1411-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1411-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="a1411-115">0x8007202F</span></span></td>
<td><span data-ttu-id="a1411-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>。</span><span class="sxs-lookup"><span data-stu-id="a1411-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="a1411-117">如果您嘗試將安全性群組新增至以混合模式執行之網域中的另一個群組，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1411-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="a1411-118">安全性群組無法以混合模式來嵌套;安全性群組只能以原生模式進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="a1411-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




