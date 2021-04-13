---
title: ConfidenceText 屬性
description: ConfidenceText 屬性
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375164"
---
# <a name="confidencetext-property"></a><span data-ttu-id="24f56-103">ConfidenceText 屬性</span><span class="sxs-lookup"><span data-stu-id="24f56-103">ConfidenceText Property</span></span>

<span data-ttu-id="24f56-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="24f56-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="24f56-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="24f56-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="24f56-106">傳回或設定出現在接聽提示中的用戶端 **ConfidenceText** 。</span><span class="sxs-lookup"><span data-stu-id="24f56-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="24f56-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="24f56-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="24f56-108">\* 代理程式 ***。 (***"CharacterID ***" ) 的字元。命令 ( "*** name \***" )**。 \[ ConfidenceText  = *字串*\]</span><span class="sxs-lookup"><span data-stu-id="24f56-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="24f56-109">部分</span><span class="sxs-lookup"><span data-stu-id="24f56-109">Part</span></span>     | <span data-ttu-id="24f56-110">描述</span><span class="sxs-lookup"><span data-stu-id="24f56-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f56-111">*string*</span><span class="sxs-lookup"><span data-stu-id="24f56-111">*string*</span></span> | <span data-ttu-id="24f56-112">評估為 [**命令**](/windows/desktop/lwef/the-command-object)之 **ConfidenceText** 文字的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="24f56-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24f56-113">備註</span><span class="sxs-lookup"><span data-stu-id="24f56-113">Remarks</span></span>

<span data-ttu-id="24f56-114">當最符合 (Userinput> 的信賴) 不超過 [**信賴**](confidence-property.md) 設定時，伺服器會在接聽提示中顯示在 **ConfidenceText** 中提供的文字。</span><span class="sxs-lookup"><span data-stu-id="24f56-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 