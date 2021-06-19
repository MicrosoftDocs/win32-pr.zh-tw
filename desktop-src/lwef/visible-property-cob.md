---
title: 'Visible 屬性 (字元物件) '
description: 深入瞭解字元物件的 Visible 屬性，它會傳回布林值，指出是否可以看見該字元。
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396303"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="b812b-103">Visible 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="b812b-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="b812b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b812b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b812b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="b812b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b812b-106">傳回布林值，指出字元是否可見。</span><span class="sxs-lookup"><span data-stu-id="b812b-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="b812b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="b812b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="b812b-108">\*代理程式 \***。 (**"\* CharacterID *" \* \* 的字元 ) 。可見*\*</span><span class="sxs-lookup"><span data-stu-id="b812b-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="b812b-109">值</span><span class="sxs-lookup"><span data-stu-id="b812b-109">Value</span></span> | <span data-ttu-id="b812b-110">描述</span><span class="sxs-lookup"><span data-stu-id="b812b-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="b812b-111">True</span><span class="sxs-lookup"><span data-stu-id="b812b-111">True</span></span>  | <span data-ttu-id="b812b-112">字元隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="b812b-112">The character is displayed.</span></span>            |
| <span data-ttu-id="b812b-113">False</span><span class="sxs-lookup"><span data-stu-id="b812b-113">False</span></span> | <span data-ttu-id="b812b-114">隱藏的字元 (看不到) 。</span><span class="sxs-lookup"><span data-stu-id="b812b-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b812b-115">備註</span><span class="sxs-lookup"><span data-stu-id="b812b-115">Remarks</span></span>

<span data-ttu-id="b812b-116">這個屬性會指出是否顯示字元的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b812b-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="b812b-117">這並不一定表示螢幕上有影像。</span><span class="sxs-lookup"><span data-stu-id="b812b-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="b812b-118">例如，即使字元位於可見的顯示區域或目前的字元框架未包含影像時，這個屬性也會傳回 **True** 。</span><span class="sxs-lookup"><span data-stu-id="b812b-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="b812b-119">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="b812b-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="b812b-120">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="b812b-120">This property is read-only.</span></span> <span data-ttu-id="b812b-121">若要讓字元變成可見或隱藏，請使用 [**顯示**](show-method.md) 或 [**隱藏**](https://www.bing.com/search?q=**Hide**) 方法。</span><span class="sxs-lookup"><span data-stu-id="b812b-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




