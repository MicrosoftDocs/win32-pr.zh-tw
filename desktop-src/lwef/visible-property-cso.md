---
title: 'Visible 屬性 (命令物件) '
description: 瞭解命令物件的 Visible 屬性，判斷命令集合的標題是否出現在字元的快顯功能表中。
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396253"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="4a604-103">Visible 屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="4a604-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="4a604-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4a604-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4a604-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="4a604-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4a604-106">傳回或設定值，這個值會決定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的標題是否出現在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="4a604-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="4a604-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="4a604-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="4a604-108">\*代理程式 \***。 (**"\* CharacterID *" \* \* ) 的字元。可見的* \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="4a604-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="4a604-109">部分</span><span class="sxs-lookup"><span data-stu-id="4a604-109">Part</span></span>      | <span data-ttu-id="4a604-110">描述</span><span class="sxs-lookup"><span data-stu-id="4a604-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a604-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="4a604-111">*boolean*</span></span> | <span data-ttu-id="4a604-112">布林運算式，指定您的 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件是否出現在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="4a604-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="4a604-113">**True** 標題隨即出現。</span><span class="sxs-lookup"><span data-stu-id="4a604-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="4a604-114">**False** 標題不會出現。</span><span class="sxs-lookup"><span data-stu-id="4a604-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a604-115">備註</span><span class="sxs-lookup"><span data-stu-id="4a604-115">Remarks</span></span>

<span data-ttu-id="4a604-116">當您的應用程式不是輸入-主動用戶端時，標題會出現在字元的快顯功能表中，必須將這個屬性設定為 **True** ，並針對您的命令集合設定 [**caption**](caption-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4a604-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="4a604-117">此外，當您的應用程式為輸入-主動時，您集合中的命令也必須將此屬性設定為 **True** ，才會出現在快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="4a604-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

