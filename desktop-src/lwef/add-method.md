---
title: 新增方法
description: 新增方法
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021336"
---
# <a name="add-method"></a><span data-ttu-id="c2203-103">新增方法</span><span class="sxs-lookup"><span data-stu-id="c2203-103">Add Method</span></span>

<span data-ttu-id="c2203-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c2203-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c2203-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="c2203-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c2203-106">將 [命令](the-command-object.md) 物件加入至 [命令](the-commands-collection-object.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="c2203-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="c2203-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="c2203-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c2203-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 命令。新增* \*  *名稱*、*標題*、*語音*、*啟用*、*可見\*</span><span class="sxs-lookup"><span data-stu-id="c2203-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="c2203-109">部分</span><span class="sxs-lookup"><span data-stu-id="c2203-109">Part</span></span>      | <span data-ttu-id="c2203-110">描述</span><span class="sxs-lookup"><span data-stu-id="c2203-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2203-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="c2203-111">*Name*</span></span>    | <span data-ttu-id="c2203-112">必要。</span><span class="sxs-lookup"><span data-stu-id="c2203-112">Required.</span></span> <span data-ttu-id="c2203-113">字串值，對應至您為命令指派的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2203-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="c2203-114">*標題*</span><span class="sxs-lookup"><span data-stu-id="c2203-114">*Caption*</span></span> | <span data-ttu-id="c2203-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2203-115">Optional.</span></span> <span data-ttu-id="c2203-116">當用戶端應用程式為輸入-主動時，對應至將出現在字元快顯功能表和 [命令] 視窗中之名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="c2203-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="c2203-117">如需詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Caption](caption-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2203-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="c2203-118">*語音*</span><span class="sxs-lookup"><span data-stu-id="c2203-118">*Voice*</span></span>   | <span data-ttu-id="c2203-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2203-119">Optional.</span></span> <span data-ttu-id="c2203-120">字串值，對應于語音引擎用來辨識此命令的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="c2203-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="c2203-121">如需格式化字串替代專案的詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Voice](voice-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2203-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="c2203-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="c2203-122">*Enabled*</span></span> | <span data-ttu-id="c2203-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2203-123">Optional.</span></span> <span data-ttu-id="c2203-124">指出是否已啟用命令的布林值。</span><span class="sxs-lookup"><span data-stu-id="c2203-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="c2203-125">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="c2203-125">The default value is **True**.</span></span> <span data-ttu-id="c2203-126">如需詳細資訊，請參閱 [Command](the-command-object.md) 物件的 [Enabled](enabled-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2203-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="c2203-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="c2203-127">*Visible*</span></span> | <span data-ttu-id="c2203-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c2203-128">Optional.</span></span> <span data-ttu-id="c2203-129">布林值，指出當用戶端應用程式為輸入-主動時，命令是否會顯示在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="c2203-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="c2203-130">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="c2203-130">The default value is **True**.</span></span> <span data-ttu-id="c2203-131">如需詳細資訊，請參閱 [命令](the-command-object.md) 物件的 [Visible](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2203-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2203-132">備註</span><span class="sxs-lookup"><span data-stu-id="c2203-132">Remarks</span></span>

<span data-ttu-id="c2203-133">[命令](the-command-object.md)物件的 [[名稱](name-property.md)] 屬性值在其[命令](the-commands-collection-object.md)集合中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c2203-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="c2203-134">您必須先移除命令，才能使用相同的 [名稱] 屬性設定來建立新的命令。</span><span class="sxs-lookup"><span data-stu-id="c2203-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="c2203-135">嘗試以已存在的名稱屬性建立命令會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2203-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="c2203-136">這個方法也會傳回 [Command](the-command-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c2203-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="c2203-137">這可讓您在呼叫 .Validator.addmethod 時宣告物件，並將命令指派給它。</span><span class="sxs-lookup"><span data-stu-id="c2203-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="c2203-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2203-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2203-139">**Insert 方法**</span><span class="sxs-lookup"><span data-stu-id="c2203-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="c2203-140">**RemoveAll 方法**</span><span class="sxs-lookup"><span data-stu-id="c2203-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="c2203-141">**Remove 方法**</span><span class="sxs-lookup"><span data-stu-id="c2203-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




