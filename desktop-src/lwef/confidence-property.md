---
title: 信賴屬性
description: 信賴屬性
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375037"
---
# <a name="confidence-property"></a><span data-ttu-id="f4d1f-103">信賴屬性</span><span class="sxs-lookup"><span data-stu-id="f4d1f-103">Confidence Property</span></span>

<span data-ttu-id="f4d1f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f4d1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f4d1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="f4d1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f4d1f-106">傳回或設定用戶端的 **信賴度** 是否出現在接聽提示中。</span><span class="sxs-lookup"><span data-stu-id="f4d1f-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="f4d1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="f4d1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f4d1f-108">\*代理程式 ***。 (***"CharacterID ***" ) 的字元。命令 ( "*** name \***" )**. \* \* 信賴\* \*  \[  =  *號碼*\]</span><span class="sxs-lookup"><span data-stu-id="f4d1f-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="f4d1f-109">部分</span><span class="sxs-lookup"><span data-stu-id="f4d1f-109">Part</span></span>     | <span data-ttu-id="f4d1f-110">描述</span><span class="sxs-lookup"><span data-stu-id="f4d1f-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d1f-111">*Number*</span><span class="sxs-lookup"><span data-stu-id="f4d1f-111">*Number*</span></span> | <span data-ttu-id="f4d1f-112">評估為長整數的數值運算式，可識別 [**命令**](/windows/desktop/lwef/the-command-object)的信賴值。</span><span class="sxs-lookup"><span data-stu-id="f4d1f-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4d1f-113">備註</span><span class="sxs-lookup"><span data-stu-id="f4d1f-113">Remarks</span></span>

<span data-ttu-id="f4d1f-114">如果最符合的傳回信賴值 (Userinput>。信賴) 不會超過您為 **信賴** 屬性設定的值，則 [**ConfidenceText**](confidencetext-property.md) 中提供的文字會顯示在接聽提示中。</span><span class="sxs-lookup"><span data-stu-id="f4d1f-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 