---
title: HasOtherClients 屬性
description: HasOtherClients 屬性
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021478"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="ee68b-103">HasOtherClients 屬性</span><span class="sxs-lookup"><span data-stu-id="ee68b-103">HasOtherClients Property</span></span>

<span data-ttu-id="ee68b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ee68b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ee68b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="ee68b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ee68b-106">傳回指定的字元是否正由其他應用程式使用中。</span><span class="sxs-lookup"><span data-stu-id="ee68b-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="ee68b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="ee68b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ee68b-108">*代理程式*。**( "***CharacterID***" ) 的字元。HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="ee68b-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="ee68b-109">值</span><span class="sxs-lookup"><span data-stu-id="ee68b-109">Value</span></span>     | <span data-ttu-id="ee68b-110">描述</span><span class="sxs-lookup"><span data-stu-id="ee68b-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="ee68b-111">**True**</span><span class="sxs-lookup"><span data-stu-id="ee68b-111">**True**</span></span>  | <span data-ttu-id="ee68b-112">字元有其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="ee68b-112">The character has other clients.</span></span>           |
| <span data-ttu-id="ee68b-113">**False**</span><span class="sxs-lookup"><span data-stu-id="ee68b-113">**False**</span></span> | <span data-ttu-id="ee68b-114">字元沒有其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="ee68b-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee68b-115">備註</span><span class="sxs-lookup"><span data-stu-id="ee68b-115">Remarks</span></span>

<span data-ttu-id="ee68b-116">當有多個應用程式正在共用 (載入) 相同的字元時，您可以使用這個屬性來判斷您的應用程式是否為唯一的字元或最後一個用戶端。</span><span class="sxs-lookup"><span data-stu-id="ee68b-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




