---
description: 根據指定的旗標，控制 WMI 建立或更新類別的方式。
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996626"
---
# <a name="pragma-classflags"></a><span data-ttu-id="6d51d-103">pragma classflags</span><span class="sxs-lookup"><span data-stu-id="6d51d-103">pragma classflags</span></span>

<span data-ttu-id="6d51d-104">**Pragma classflags** 預處理器命令會根據指定的旗標，控制 WMI 建立或更新類別的方式。</span><span class="sxs-lookup"><span data-stu-id="6d51d-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="6d51d-105">以下說明此命令的語法：</span><span class="sxs-lookup"><span data-stu-id="6d51d-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="6d51d-106">*\[ 旗 \]* 標必須是下列一個或多個引數。</span><span class="sxs-lookup"><span data-stu-id="6d51d-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="6d51d-107">您可以結合彼此不互相矛盾的旗標。</span><span class="sxs-lookup"><span data-stu-id="6d51d-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="6d51d-108">旗標</span><span class="sxs-lookup"><span data-stu-id="6d51d-108">Flag</span></span>        | <span data-ttu-id="6d51d-109">描述</span><span class="sxs-lookup"><span data-stu-id="6d51d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d51d-110">以</span><span class="sxs-lookup"><span data-stu-id="6d51d-110">createonly</span></span>  | <span data-ttu-id="6d51d-111">指示編譯器不要對現有的類別進行任何變更，而且如果在 MOF 檔案中指定的類別已經存在於 WMI 中，就會終止編譯。</span><span class="sxs-lookup"><span data-stu-id="6d51d-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="6d51d-112">forceupdate</span><span class="sxs-lookup"><span data-stu-id="6d51d-112">forceupdate</span></span> | <span data-ttu-id="6d51d-113">存在衝突的子類別時，強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="6d51d-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="6d51d-114">例如，如果您在子類別中定義類別辨識符號，而基類嘗試加入相同的辨識符號，使用此旗標會在子類別中刪除衝突的辨識符號，以使編譯器解決此衝突。</span><span class="sxs-lookup"><span data-stu-id="6d51d-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="6d51d-115">如果子類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="6d51d-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="6d51d-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="6d51d-116">safeupdate</span></span>  | <span data-ttu-id="6d51d-117">即使子類別存在，也允許編譯器更新類別（如果變更不會造成與子類別的衝突）。</span><span class="sxs-lookup"><span data-stu-id="6d51d-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="6d51d-118">例如，這個旗標可讓您將新的屬性新增至基類，而不需要將屬性新增至任何既有的子類別。</span><span class="sxs-lookup"><span data-stu-id="6d51d-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="6d51d-119">如果子類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="6d51d-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="6d51d-120">updateonly</span><span class="sxs-lookup"><span data-stu-id="6d51d-120">updateonly</span></span>  | <span data-ttu-id="6d51d-121">指示編譯器不要建立任何新的類別，而且如果 MOF 檔案中指定的類別不存在，編譯器就會終止編譯。</span><span class="sxs-lookup"><span data-stu-id="6d51d-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="6d51d-122">範例</span><span class="sxs-lookup"><span data-stu-id="6d51d-122">Examples</span></span>

<span data-ttu-id="6d51d-123">下列範例示範如何使用此命令搭配 updateonly 和 forceupdate 旗標。</span><span class="sxs-lookup"><span data-stu-id="6d51d-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="6d51d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d51d-124">Requirements</span></span>



| <span data-ttu-id="6d51d-125">需求</span><span class="sxs-lookup"><span data-stu-id="6d51d-125">Requirement</span></span> | <span data-ttu-id="6d51d-126">值</span><span class="sxs-lookup"><span data-stu-id="6d51d-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6d51d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d51d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d51d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d51d-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6d51d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d51d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d51d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d51d-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d51d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d51d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d51d-132">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="6d51d-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




