---
title: Insert 方法
description: Insert 方法
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966240"
---
# <a name="insert-method"></a><span data-ttu-id="739bc-103">Insert 方法</span><span class="sxs-lookup"><span data-stu-id="739bc-103">Insert Method</span></span>

<span data-ttu-id="739bc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="739bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="739bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="739bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-106">在 **命令** 集合中插入 **Command** 物件。</span><span class="sxs-lookup"><span data-stu-id="739bc-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="739bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="739bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 命令。 Insert* \*  *Name*， *RefName*， *Before*\_</span><span class="sxs-lookup"><span data-stu-id="739bc-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="739bc-109">*標題*、 *語音、啟用、可見*</span><span class="sxs-lookup"><span data-stu-id="739bc-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="739bc-110">部分</span><span class="sxs-lookup"><span data-stu-id="739bc-110">Part</span></span>      | <span data-ttu-id="739bc-111">描述</span><span class="sxs-lookup"><span data-stu-id="739bc-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="739bc-112">*名稱*</span><span class="sxs-lookup"><span data-stu-id="739bc-112">*Name*</span></span>    | <span data-ttu-id="739bc-113">必要。</span><span class="sxs-lookup"><span data-stu-id="739bc-113">Required.</span></span> <span data-ttu-id="739bc-114">字串值，對應至您指派給 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。</span><span class="sxs-lookup"><span data-stu-id="739bc-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="739bc-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="739bc-115">*RefName*</span></span> | <span data-ttu-id="739bc-116">必要。</span><span class="sxs-lookup"><span data-stu-id="739bc-116">Required.</span></span> <span data-ttu-id="739bc-117">字串值，對應至您要插入新命令的上方或下方命令的名稱 (識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="739bc-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="739bc-118">*之前*</span><span class="sxs-lookup"><span data-stu-id="739bc-118">*Before*</span></span>  | <span data-ttu-id="739bc-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="739bc-119">Optional.</span></span> <span data-ttu-id="739bc-120">布林值，指出是否要在 *RefName* 指定的命令之前插入新的命令。</span><span class="sxs-lookup"><span data-stu-id="739bc-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="739bc-121">**True** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="739bc-121">**True** (Default).</span></span> <span data-ttu-id="739bc-122">新的命令會在參考的命令之前插入。</span><span class="sxs-lookup"><span data-stu-id="739bc-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="739bc-123">**False** 新的命令會在參考的命令之後插入。</span><span class="sxs-lookup"><span data-stu-id="739bc-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="739bc-124">*標題*</span><span class="sxs-lookup"><span data-stu-id="739bc-124">*Caption*</span></span> | <span data-ttu-id="739bc-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="739bc-125">Optional.</span></span> <span data-ttu-id="739bc-126">當用戶端應用程式為輸入-主動時，對應至將出現在字元快顯功能表和 [命令] 視窗中之名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="739bc-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="739bc-127">如需詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Caption**](caption-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="739bc-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="739bc-128">*語音*</span><span class="sxs-lookup"><span data-stu-id="739bc-128">*Voice*</span></span>   | <span data-ttu-id="739bc-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="739bc-129">Optional.</span></span> <span data-ttu-id="739bc-130">字串值，對應于語音引擎用來辨識此命令的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="739bc-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="739bc-131">如需格式化字串替代專案的詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 **Voice** 屬性。</span><span class="sxs-lookup"><span data-stu-id="739bc-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="739bc-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="739bc-132">*Enabled*</span></span> | <span data-ttu-id="739bc-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="739bc-133">Optional.</span></span> <span data-ttu-id="739bc-134">指出是否已啟用命令的布林值。</span><span class="sxs-lookup"><span data-stu-id="739bc-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="739bc-135">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="739bc-135">The default value is **True**.</span></span> <span data-ttu-id="739bc-136">如需詳細資訊，請參閱 [**Command**](/windows/desktop/lwef/the-command-object) 物件的 **Enabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="739bc-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="739bc-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="739bc-137">*Visible*</span></span> | <span data-ttu-id="739bc-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="739bc-138">Optional.</span></span> <span data-ttu-id="739bc-139">指出當用戶端應用程式為輸入-主動時，命令視窗中是否顯示命令的布林值。</span><span class="sxs-lookup"><span data-stu-id="739bc-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="739bc-140">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="739bc-140">The default value is **True**.</span></span> <span data-ttu-id="739bc-141">如需詳細資訊，請參閱 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="739bc-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="739bc-142">備註</span><span class="sxs-lookup"><span data-stu-id="739bc-142">Remarks</span></span>

<span data-ttu-id="739bc-143">[**命令**](/windows/desktop/lwef/the-command-object)物件的 [[**名稱**](name-property.md)] 屬性值在其 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="739bc-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="739bc-144">您必須先移除 **命令**，才能使用相同的 [**名稱**] 屬性設定來建立新的 **命令**。</span><span class="sxs-lookup"><span data-stu-id="739bc-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="739bc-145">嘗試以已存在的 **名稱** 屬性建立 **命令** 會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="739bc-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="739bc-146">這個方法也會傳回 [**Command**](/windows/desktop/lwef/the-command-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="739bc-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="739bc-147">這可讓您宣告物件，並在呼叫 **Insert** 方法時將 **命令** 指派給它。</span><span class="sxs-lookup"><span data-stu-id="739bc-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="739bc-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="739bc-148">See Also</span></span>

<span data-ttu-id="739bc-149">[**Add 方法**](add-method.md)、 [**Remove 方法**](remove-method.md)、 [**RemoveAll 方法**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="739bc-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

