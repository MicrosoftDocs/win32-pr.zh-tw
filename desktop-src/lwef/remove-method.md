---
title: Remove 方法
description: Remove 方法
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315136"
---
# <a name="remove-method"></a><span data-ttu-id="8c647-103">Remove 方法</span><span class="sxs-lookup"><span data-stu-id="8c647-103">Remove Method</span></span>

<span data-ttu-id="8c647-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8c647-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8c647-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="8c647-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8c647-106">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除 [**Command**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="8c647-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="8c647-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="8c647-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8c647-108">*代理程式 ***。 ( "*** CharacterID" 的字元 ***) 命令。移除*** 名稱*</span><span class="sxs-lookup"><span data-stu-id="8c647-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="8c647-109">部分</span><span class="sxs-lookup"><span data-stu-id="8c647-109">Part</span></span>   | <span data-ttu-id="8c647-110">描述</span><span class="sxs-lookup"><span data-stu-id="8c647-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="8c647-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="8c647-111">*Name*</span></span> | <span data-ttu-id="8c647-112">必要。</span><span class="sxs-lookup"><span data-stu-id="8c647-112">Required.</span></span> <span data-ttu-id="8c647-113">與命令的識別碼對應的字串值。</span><span class="sxs-lookup"><span data-stu-id="8c647-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c647-114">備註</span><span class="sxs-lookup"><span data-stu-id="8c647-114">Remarks</span></span>

<span data-ttu-id="8c647-115">從集合中移除 [**命令**](/windows/desktop/lwef/the-command-object) 物件時，當您的用戶端應用程式為輸入使用中時，它就不會再顯示。</span><span class="sxs-lookup"><span data-stu-id="8c647-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c647-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c647-116">See Also</span></span>

[<span data-ttu-id="8c647-117">**RemoveAll 方法**</span><span class="sxs-lookup"><span data-stu-id="8c647-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 