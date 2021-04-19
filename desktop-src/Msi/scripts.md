---
description: 自訂動作可以呼叫以 VBScript 或 JScript 撰寫的函式。
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: 指令碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993140"
---
# <a name="scripts"></a><span data-ttu-id="ea703-103">指令碼</span><span class="sxs-lookup"><span data-stu-id="ea703-103">Scripts</span></span>

<span data-ttu-id="ea703-104">自訂動作可以呼叫以 VBScript 或 JScript 撰寫的函式。</span><span class="sxs-lookup"><span data-stu-id="ea703-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="ea703-105">Windows Installer 不提供腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="ea703-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="ea703-106">因此，想要在安裝期間利用指令碼語言的作者，必須確保適當的腳本引擎可以使用。</span><span class="sxs-lookup"><span data-stu-id="ea703-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="ea703-107">安裝程式不支援 JScript 1.0 版。</span><span class="sxs-lookup"><span data-stu-id="ea703-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="ea703-108">以腳本為基礎的64位自訂動作必須明確標記為64位自訂動作，方法是在 [CustomAction](customaction-table.md)資料表的類型資料行中，將 **msidbCustomActionType64BitScript** 位新增至自訂動作數數值型別。</span><span class="sxs-lookup"><span data-stu-id="ea703-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="ea703-109">如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="ea703-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="ea703-110">下列基本自訂動作類型會呼叫以腳本撰寫的函式。</span><span class="sxs-lookup"><span data-stu-id="ea703-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="ea703-111">自訂動作類型</span><span class="sxs-lookup"><span data-stu-id="ea703-111">Custom action type</span></span>                                 | <span data-ttu-id="ea703-112">Description</span><span class="sxs-lookup"><span data-stu-id="ea703-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea703-113">自訂動作類型5</span><span class="sxs-lookup"><span data-stu-id="ea703-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="ea703-114">二進位資料表資料流程中儲存的 JScript 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea703-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="ea703-115">自訂動作類型21</span><span class="sxs-lookup"><span data-stu-id="ea703-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="ea703-116">隨產品安裝的 JScript 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea703-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="ea703-117">自訂動作類型53</span><span class="sxs-lookup"><span data-stu-id="ea703-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="ea703-118">由屬性值指定的 JScript 文字。</span><span class="sxs-lookup"><span data-stu-id="ea703-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="ea703-119">自訂動作類型37</span><span class="sxs-lookup"><span data-stu-id="ea703-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="ea703-120">儲存在 [CustomAction](customaction-table.md) 資料表的目標資料行中的 JScript 文字。</span><span class="sxs-lookup"><span data-stu-id="ea703-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="ea703-121">自訂動作類型6</span><span class="sxs-lookup"><span data-stu-id="ea703-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="ea703-122">儲存在 [二進位](binary-table.md) 資料表資料流程中的 VBScript 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea703-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="ea703-123">自訂動作類型22</span><span class="sxs-lookup"><span data-stu-id="ea703-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="ea703-124">隨產品安裝的 VBScript 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea703-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="ea703-125">自訂動作類型54</span><span class="sxs-lookup"><span data-stu-id="ea703-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="ea703-126">由屬性值指定的 VBScript 文字。</span><span class="sxs-lookup"><span data-stu-id="ea703-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="ea703-127">自訂動作類型38</span><span class="sxs-lookup"><span data-stu-id="ea703-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="ea703-128">[CustomAction](customaction-table.md)資料表的目標資料行中所儲存的 VBScript 文字。</span><span class="sxs-lookup"><span data-stu-id="ea703-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ea703-129">安裝程式會直接執行腳本自訂動作，而不會使用 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="ea703-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="ea703-130">無法在腳本自訂動作內使用 **wscript.echo** 物件，因為此物件是由 Windows script Host 提供。</span><span class="sxs-lookup"><span data-stu-id="ea703-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="ea703-131">Windows Script Host 物件模型中的物件，只能在自訂動作中使用：如果在電腦上安裝 Windows Script Host，只要建立物件的新實例、呼叫 CreateObject，並提供物件的 ProgId (例如 "Wscript.echo" ) 。</span><span class="sxs-lookup"><span data-stu-id="ea703-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="ea703-132">根據腳本的自訂動作類型而定，基於安全性考慮，可能會拒絕存取 Windows Script Host 物件模型的某些物件和方法。</span><span class="sxs-lookup"><span data-stu-id="ea703-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="ea703-133">如需詳細資訊，請參閱所有自訂動作 [類型的摘要清單](summary-list-of-all-custom-action-types.md) ，以取得所有自訂動作類型的摘要，以及它們如何編碼至 [CustomAction](customaction-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="ea703-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



