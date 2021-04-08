---
title: RemoveAll 方法
description: RemoveAll 方法
ms.assetid: 233f8d65-36ec-4c83-8c91-59d406edd70a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56a22536d2d481f9da0073265e529b9a73a4088
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933244"
---
# <a name="removeall-method"></a><span data-ttu-id="c5a10-103">RemoveAll 方法</span><span class="sxs-lookup"><span data-stu-id="c5a10-103">RemoveAll Method</span></span>

<span data-ttu-id="c5a10-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c5a10-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c5a10-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="c5a10-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c5a10-106">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除所有的 [**命令**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="c5a10-106">Removes all [**Command**](/windows/desktop/lwef/the-command-object) objects from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="c5a10-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="c5a10-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c5a10-108">*代理程式 ***。字元 ( "*** CharacterID \* \* *" ) . RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="c5a10-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.RemoveAll*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5a10-109">備註</span><span class="sxs-lookup"><span data-stu-id="c5a10-109">Remarks</span></span>

<span data-ttu-id="c5a10-110">從集合中移除 [**命令**](/windows/desktop/lwef/the-command-object) 物件時，當您的用戶端應用程式為輸入使用中時，它就不會再顯示。</span><span class="sxs-lookup"><span data-stu-id="c5a10-110">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5a10-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5a10-111">See Also</span></span>

[<span data-ttu-id="c5a10-112">**Remove 方法**</span><span class="sxs-lookup"><span data-stu-id="c5a10-112">**Remove method**</span></span>](remove-method.md)


 

 