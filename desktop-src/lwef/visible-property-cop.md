---
title: 'Visible 屬性 (Command 物件) '
description: Visible 屬性
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106984947"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="3758d-103">Visible 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="3758d-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="3758d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3758d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3758d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="3758d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3758d-106">傳回或設定 [**命令**](/windows/desktop/lwef/the-command-object) 是否顯示在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="3758d-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="3758d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3758d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="3758d-108">\*代理程式 \***。字元 (**"\* CharacterID *"**) . 命令 (**"* name *" \* \* ) 。可見* 的 \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="3758d-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="3758d-109">部分</span><span class="sxs-lookup"><span data-stu-id="3758d-109">Part</span></span>      | <span data-ttu-id="3758d-110">描述</span><span class="sxs-lookup"><span data-stu-id="3758d-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3758d-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="3758d-111">*boolean*</span></span> | <span data-ttu-id="3758d-112">布林運算式，指定是否要在字元的快顯功能表中出現 [**命令**](/windows/desktop/lwef/the-command-object)的標題。</span><span class="sxs-lookup"><span data-stu-id="3758d-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="3758d-113">**True** (預設) 標題隨即出現。</span><span class="sxs-lookup"><span data-stu-id="3758d-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="3758d-114">**False** 標題不會出現。</span><span class="sxs-lookup"><span data-stu-id="3758d-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3758d-115">備註</span><span class="sxs-lookup"><span data-stu-id="3758d-115">Remarks</span></span>

<span data-ttu-id="3758d-116">當您想要包含自己介面的語音輸入，而不將其顯示在字元的快顯功能表中時，請將此屬性設定為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="3758d-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="3758d-117">如果您將 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Caption**](caption-property.md) 屬性設為空字串 ( "" ) ，標題文字就不會出現在快顯功能表中 (例如，不論它的 [**Visible**](visible-property.md) 屬性設定為何，都不會出現在快顯功能表中例如空白行) 。</span><span class="sxs-lookup"><span data-stu-id="3758d-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="3758d-118">[**命令**](/windows/desktop/lwef/the-command-object)物件之父 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**visible**](visible-property.md)屬性設定，不會影響 **命令** 的 **visible** 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="3758d-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

