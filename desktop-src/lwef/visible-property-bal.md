---
title: 'Visible 屬性 (Balloon 物件) '
description: Visible 屬性
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024397"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="17ea3-103">Visible 屬性 (Balloon 物件) </span><span class="sxs-lookup"><span data-stu-id="17ea3-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="17ea3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="17ea3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17ea3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="17ea3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17ea3-106">針對指定的字元，傳回或設定文字批註的可見設定。</span><span class="sxs-lookup"><span data-stu-id="17ea3-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="17ea3-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="17ea3-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="17ea3-108">\*代理程式 \***。 (**"\* CharacterID *" \* \* 的字元 ) 。球形提示。可見的* \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="17ea3-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="17ea3-109">部分</span><span class="sxs-lookup"><span data-stu-id="17ea3-109">Part</span></span>      | <span data-ttu-id="17ea3-110">描述</span><span class="sxs-lookup"><span data-stu-id="17ea3-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ea3-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="17ea3-111">*boolean*</span></span> | <span data-ttu-id="17ea3-112">布林運算式，指定是否顯示文字提示。</span><span class="sxs-lookup"><span data-stu-id="17ea3-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="17ea3-113">**True** 氣球是可見的。</span><span class="sxs-lookup"><span data-stu-id="17ea3-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="17ea3-114">**False** 這個氣球是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="17ea3-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17ea3-115">備註</span><span class="sxs-lookup"><span data-stu-id="17ea3-115">Remarks</span></span>

<span data-ttu-id="17ea3-116">如果您遵循 [**說**](speak-method.md)出或使用語句來嘗試變更氣球的屬性，它可能不會影響氣球的可見狀態，因為 **說** 出或 **思考** 呼叫會排入佇列，但呼叫設定球的可見狀態則不 [**會這麼做**](think-method.md)。</span><span class="sxs-lookup"><span data-stu-id="17ea3-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="17ea3-117">因此，只有在字元的佇列中沒有 **說話** 或 **思考** 電話時，才會設定此值。</span><span class="sxs-lookup"><span data-stu-id="17ea3-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="17ea3-118">如果您嘗試在字元是說話、移動或拖曳時設定這個屬性，則在先前的作業完成之前，屬性設定不會生效。</span><span class="sxs-lookup"><span data-stu-id="17ea3-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="17ea3-119">呼叫「 [**說話**](speak-method.md) 」和「 [**想法**](think-method.md) 」方法會自動使球顯示，將 [**visible**](visible-property.md) 屬性設為 **True**。</span><span class="sxs-lookup"><span data-stu-id="17ea3-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="17ea3-120">如果已啟用字元的 [自動隱藏隱藏] 屬性，則會在讀出輸出文字之後，自動隱藏球。</span><span class="sxs-lookup"><span data-stu-id="17ea3-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="17ea3-121">按一下或拖曳目前未說話的字元也會自動隱藏球標，即使停用自動隱藏設定也是如此。</span><span class="sxs-lookup"><span data-stu-id="17ea3-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="17ea3-122">您可以使用氣球的 [**Style**](style-property.md) 屬性來變更字元的 [自動隱藏] 設定。</span><span class="sxs-lookup"><span data-stu-id="17ea3-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="17ea3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17ea3-123">See Also</span></span>

[<span data-ttu-id="17ea3-124">**Style 屬性**</span><span class="sxs-lookup"><span data-stu-id="17ea3-124">**Style property**</span></span>](style-property.md)


 

 





