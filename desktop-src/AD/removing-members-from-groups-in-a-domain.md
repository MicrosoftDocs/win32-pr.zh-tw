---
title: 移除網域中群組的成員
description: 您可以從群組中移除使用者、群組或連絡人。
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- 群組 AD，移除網域中群組的成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681644"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="15078-104">移除網域中群組的成員</span><span class="sxs-lookup"><span data-stu-id="15078-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="15078-105">您可以從群組中移除使用者、群組或連絡人。</span><span class="sxs-lookup"><span data-stu-id="15078-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="15078-106">**群組** 物件的 **成員** 屬性包含群組的所有直接成員。</span><span class="sxs-lookup"><span data-stu-id="15078-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="15078-107">從群組中移除成員最簡單的方法，就是在您想要從中移除成員的群組物件的 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)介面上，呼叫 [**IADsGroup。**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove)</span><span class="sxs-lookup"><span data-stu-id="15078-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 