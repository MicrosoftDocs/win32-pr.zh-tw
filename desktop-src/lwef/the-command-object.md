---
title: Command 物件
description: Command 物件
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967890"
---
# <a name="the-command-object"></a><span data-ttu-id="09bdb-103">Command 物件</span><span class="sxs-lookup"><span data-stu-id="09bdb-103">The Command Object</span></span>

<span data-ttu-id="09bdb-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="09bdb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="09bdb-105">[**命令**](/windows/desktop/lwef/the-command-object)物件是 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="09bdb-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="09bdb-106">當您的用戶端應用程式變成輸入-主動時，伺服器會為使用者提供 **命令** 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="09bdb-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="09bdb-107">Command 物件屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="09bdb-108">若要存取 [**命令**](/windows/desktop/lwef/the-command-object) 物件的屬性，請使用其 [ [**名稱**](name-property.md) ] 屬性在集合中參考它。</span><span class="sxs-lookup"><span data-stu-id="09bdb-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="09bdb-109">在 VBScript 和 Visual Basic 中，您可以直接使用 **Name** 屬性：</span><span class="sxs-lookup"><span data-stu-id="09bdb-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="09bdb-110">針對不支援集合的程式設計語言，請使用 [**命令**](command-method.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="09bdb-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="09bdb-111">您也可以藉由建立命令物件的參考來參考它。</span><span class="sxs-lookup"><span data-stu-id="09bdb-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="09bdb-112">在 Visual Basic 中，宣告物件變數並使用 Set 語句來建立參考：</span><span class="sxs-lookup"><span data-stu-id="09bdb-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="09bdb-113">在 Visual Basic 5.0 中，您也可以將物件宣告為類型 [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) ，然後建立參考。</span><span class="sxs-lookup"><span data-stu-id="09bdb-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="09bdb-114">此慣例可啟用早期繫結，進而提高效能：</span><span class="sxs-lookup"><span data-stu-id="09bdb-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="09bdb-115">在 VBScript 中，您可以將參考宣告為特定類型，但是您仍然可以宣告變數，並將它設定為集合中的 [**命令**](/windows/desktop/lwef/the-command-object) ：</span><span class="sxs-lookup"><span data-stu-id="09bdb-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="09bdb-116">命令可能會出現在字元的快顯功能表和 [命令] 視窗中，或同時出現在兩者中。</span><span class="sxs-lookup"><span data-stu-id="09bdb-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="09bdb-117">若要顯示在快顯功能表中，它必須有標題，並將 [**Visible**](visible-property.md) 屬性設為 **True**。</span><span class="sxs-lookup"><span data-stu-id="09bdb-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="09bdb-118">此外，它的命令集合物件 **Visible** 屬性也必須設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="09bdb-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="09bdb-119">若要顯示在 [命令] 視窗中， [**命令**](/windows/desktop/lwef/the-command-object) 必須設定其 [**標題**](caption-property.md) 和 [**語音**](voice-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="09bdb-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="09bdb-120">請注意，當功能表顯示時，不會變更字元的快顯功能表專案。</span><span class="sxs-lookup"><span data-stu-id="09bdb-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="09bdb-121">如果您在顯示字元的快顯功能表時，新增或移除命令或變更其屬性，則當使用者下一次顯示時，功能表會顯示這些變更。</span><span class="sxs-lookup"><span data-stu-id="09bdb-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="09bdb-122">但是，命令視窗會動態反映您所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="09bdb-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="09bdb-123">下表摘要說明 [**命令**](/windows/desktop/lwef/the-command-object) 的屬性如何影響其呈現方式：</span><span class="sxs-lookup"><span data-stu-id="09bdb-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="09bdb-124">Caption 屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-124">Caption Property</span></span>

<span data-ttu-id="09bdb-125">Voice-Caption 屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-125">Voice-Caption Property</span></span>

<span data-ttu-id="09bdb-126">Voice 屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-126">Voice Property</span></span>

<span data-ttu-id="09bdb-127">Visible 屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-127">Visible Property</span></span>

<span data-ttu-id="09bdb-128">Enabled 屬性</span><span class="sxs-lookup"><span data-stu-id="09bdb-128">Enabled Property</span></span>

<span data-ttu-id="09bdb-129">出現在字元的快顯功能表中</span><span class="sxs-lookup"><span data-stu-id="09bdb-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="09bdb-130">出現在命令視窗中</span><span class="sxs-lookup"><span data-stu-id="09bdb-130">Appears in Commands Window</span></span>

<span data-ttu-id="09bdb-131">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-131">Yes</span></span>

<span data-ttu-id="09bdb-132">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-132">Yes</span></span>

<span data-ttu-id="09bdb-133">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-133">Yes</span></span>

<span data-ttu-id="09bdb-134">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-134">True</span></span>

<span data-ttu-id="09bdb-135">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-135">True</span></span>

<span data-ttu-id="09bdb-136">一般，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-137">是，使用 [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="09bdb-138">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-138">Yes</span></span>

<span data-ttu-id="09bdb-139">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-139">Yes</span></span>

<span data-ttu-id="09bdb-140">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-140">Yes</span></span>

<span data-ttu-id="09bdb-141">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-141">True</span></span>

<span data-ttu-id="09bdb-142">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-142">False</span></span>

<span data-ttu-id="09bdb-143">已停用，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-144">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-144">No</span></span>

<span data-ttu-id="09bdb-145">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-145">Yes</span></span>

<span data-ttu-id="09bdb-146">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-146">Yes</span></span>

<span data-ttu-id="09bdb-147">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-147">Yes</span></span>

<span data-ttu-id="09bdb-148">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-148">False</span></span>

<span data-ttu-id="09bdb-149">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-149">True</span></span>

<span data-ttu-id="09bdb-150">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-150">Does not appear</span></span>

<span data-ttu-id="09bdb-151">是，使用 [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="09bdb-152">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-152">Yes</span></span>

<span data-ttu-id="09bdb-153">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-153">Yes</span></span>

<span data-ttu-id="09bdb-154">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-154">Yes</span></span>

<span data-ttu-id="09bdb-155">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-155">False</span></span>

<span data-ttu-id="09bdb-156">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-156">False</span></span>

<span data-ttu-id="09bdb-157">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-157">Does not appear</span></span>

<span data-ttu-id="09bdb-158">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-158">No</span></span>

<span data-ttu-id="09bdb-159">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-159">Yes</span></span>

<span data-ttu-id="09bdb-160">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-160">Yes</span></span>

<span data-ttu-id="09bdb-161">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-161">No</span></span> 

<span data-ttu-id="09bdb-162">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-162">True</span></span>

<span data-ttu-id="09bdb-163">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-163">True</span></span>

<span data-ttu-id="09bdb-164">一般，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-165">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-165">No</span></span>

<span data-ttu-id="09bdb-166">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-166">Yes</span></span>

<span data-ttu-id="09bdb-167">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-167">Yes</span></span>

<span data-ttu-id="09bdb-168">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-168">No</span></span> 

<span data-ttu-id="09bdb-169">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-169">True</span></span>

<span data-ttu-id="09bdb-170">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-170">False</span></span>

<span data-ttu-id="09bdb-171">已停用，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-172">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-172">No</span></span>

<span data-ttu-id="09bdb-173">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-173">Yes</span></span>

<span data-ttu-id="09bdb-174">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-174">Yes</span></span>

<span data-ttu-id="09bdb-175">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-175">No</span></span> 

<span data-ttu-id="09bdb-176">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-176">False</span></span>

<span data-ttu-id="09bdb-177">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-177">True</span></span>

<span data-ttu-id="09bdb-178">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-178">Does not appear</span></span>

<span data-ttu-id="09bdb-179">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-179">No</span></span>

<span data-ttu-id="09bdb-180">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-180">Yes</span></span>

<span data-ttu-id="09bdb-181">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-181">Yes</span></span>

<span data-ttu-id="09bdb-182">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-182">No</span></span> 

<span data-ttu-id="09bdb-183">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-183">False</span></span>

<span data-ttu-id="09bdb-184">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-184">False</span></span>

<span data-ttu-id="09bdb-185">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-185">Does not appear</span></span>

<span data-ttu-id="09bdb-186">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-186">No</span></span>

<span data-ttu-id="09bdb-187">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-187">No</span></span> 

<span data-ttu-id="09bdb-188">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-188">Yes</span></span>

<span data-ttu-id="09bdb-189">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-189">Yes</span></span>

<span data-ttu-id="09bdb-190">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-190">True</span></span>

<span data-ttu-id="09bdb-191">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-191">True</span></span>

<span data-ttu-id="09bdb-192">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-192">Does not appear</span></span>

<span data-ttu-id="09bdb-193">是，使用 [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="09bdb-194">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-194">No</span></span> 

<span data-ttu-id="09bdb-195">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-195">Yes</span></span>

<span data-ttu-id="09bdb-196">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-196">Yes</span></span>

<span data-ttu-id="09bdb-197">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-197">True</span></span>

<span data-ttu-id="09bdb-198">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-198">False</span></span>

<span data-ttu-id="09bdb-199">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-199">Does not appear</span></span>

<span data-ttu-id="09bdb-200">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-200">No</span></span>

<span data-ttu-id="09bdb-201">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-201">No</span></span> 

<span data-ttu-id="09bdb-202">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-202">Yes</span></span>

<span data-ttu-id="09bdb-203">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-203">Yes</span></span>

<span data-ttu-id="09bdb-204">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-204">False</span></span>

<span data-ttu-id="09bdb-205">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-205">True</span></span>

<span data-ttu-id="09bdb-206">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-206">Does not appear</span></span>

<span data-ttu-id="09bdb-207">是，使用 [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="09bdb-208">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-208">No</span></span> 

<span data-ttu-id="09bdb-209">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-209">Yes</span></span>

<span data-ttu-id="09bdb-210">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-210">Yes</span></span>

<span data-ttu-id="09bdb-211">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-211">False</span></span>

<span data-ttu-id="09bdb-212">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-212">False</span></span>

<span data-ttu-id="09bdb-213">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-213">Does not appear</span></span>

<span data-ttu-id="09bdb-214">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-214">No</span></span>

<span data-ttu-id="09bdb-215">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-215">No</span></span> 

<span data-ttu-id="09bdb-216">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-216">Yes</span></span>

<span data-ttu-id="09bdb-217">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-217">No</span></span> 

<span data-ttu-id="09bdb-218">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-218">True</span></span>

<span data-ttu-id="09bdb-219">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-219">True</span></span>

<span data-ttu-id="09bdb-220">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-220">Does not appear</span></span>

<span data-ttu-id="09bdb-221">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-221">No</span></span>

<span data-ttu-id="09bdb-222">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-222">No</span></span> 

<span data-ttu-id="09bdb-223">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-223">Yes</span></span>

<span data-ttu-id="09bdb-224">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-224">No</span></span> 

<span data-ttu-id="09bdb-225">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-225">True</span></span>

<span data-ttu-id="09bdb-226">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-226">False</span></span>

<span data-ttu-id="09bdb-227">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-227">Does not appear</span></span>

<span data-ttu-id="09bdb-228">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-228">No</span></span>

<span data-ttu-id="09bdb-229">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-229">No</span></span> 

<span data-ttu-id="09bdb-230">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-230">Yes</span></span>

<span data-ttu-id="09bdb-231">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-231">No</span></span> 

<span data-ttu-id="09bdb-232">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-232">False</span></span>

<span data-ttu-id="09bdb-233">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-233">True</span></span>

<span data-ttu-id="09bdb-234">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-234">Does not appear</span></span>

<span data-ttu-id="09bdb-235">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-235">No</span></span>

<span data-ttu-id="09bdb-236">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-236">No</span></span> 

<span data-ttu-id="09bdb-237">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-237">Yes</span></span>

<span data-ttu-id="09bdb-238">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-238">No</span></span> 

<span data-ttu-id="09bdb-239">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-239">False</span></span>

<span data-ttu-id="09bdb-240">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-240">False</span></span>

<span data-ttu-id="09bdb-241">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-241">Does not appear</span></span>

<span data-ttu-id="09bdb-242">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-242">No</span></span>

<span data-ttu-id="09bdb-243">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-243">Yes</span></span>

<span data-ttu-id="09bdb-244">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-244">No</span></span> 

<span data-ttu-id="09bdb-245">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-245">Yes</span></span>

<span data-ttu-id="09bdb-246">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-246">True</span></span>

<span data-ttu-id="09bdb-247">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-247">True</span></span>

<span data-ttu-id="09bdb-248">一般，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-249">是，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-250">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-250">Yes</span></span>

<span data-ttu-id="09bdb-251">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-251">No</span></span> 

<span data-ttu-id="09bdb-252">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-252">Yes</span></span>

<span data-ttu-id="09bdb-253">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-253">True</span></span>

<span data-ttu-id="09bdb-254">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-254">False</span></span>

<span data-ttu-id="09bdb-255">已停用，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-256">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-256">No</span></span>

<span data-ttu-id="09bdb-257">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-257">Yes</span></span>

<span data-ttu-id="09bdb-258">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-258">No</span></span> 

<span data-ttu-id="09bdb-259">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-259">Yes</span></span>

<span data-ttu-id="09bdb-260">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-260">False</span></span>

<span data-ttu-id="09bdb-261">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-261">True</span></span>

<span data-ttu-id="09bdb-262">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-262">Does not appear</span></span>

<span data-ttu-id="09bdb-263">是，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-264">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-264">Yes</span></span>

<span data-ttu-id="09bdb-265">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-265">No</span></span> 

<span data-ttu-id="09bdb-266">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-266">Yes</span></span>

<span data-ttu-id="09bdb-267">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-267">False</span></span>

<span data-ttu-id="09bdb-268">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-268">False</span></span>

<span data-ttu-id="09bdb-269">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-269">Does not appear</span></span>

<span data-ttu-id="09bdb-270">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-270">No</span></span>

<span data-ttu-id="09bdb-271">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-271">Yes</span></span>

<span data-ttu-id="09bdb-272">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-272">No</span></span> 

<span data-ttu-id="09bdb-273">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-273">No</span></span> 

<span data-ttu-id="09bdb-274">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-274">True</span></span>

<span data-ttu-id="09bdb-275">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-275">True</span></span>

<span data-ttu-id="09bdb-276">一般，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-277">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-277">No</span></span>

<span data-ttu-id="09bdb-278">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-278">Yes</span></span>

<span data-ttu-id="09bdb-279">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-279">No</span></span> 

<span data-ttu-id="09bdb-280">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-280">No</span></span> 

<span data-ttu-id="09bdb-281">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-281">True</span></span>

<span data-ttu-id="09bdb-282">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-282">False</span></span>

<span data-ttu-id="09bdb-283">已停用，使用 [**標題**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="09bdb-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="09bdb-284">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-284">No</span></span>

<span data-ttu-id="09bdb-285">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-285">Yes</span></span>

<span data-ttu-id="09bdb-286">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-286">No</span></span> 

<span data-ttu-id="09bdb-287">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-287">No</span></span> 

<span data-ttu-id="09bdb-288">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-288">False</span></span>

<span data-ttu-id="09bdb-289">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-289">True</span></span>

<span data-ttu-id="09bdb-290">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-290">Does not appear</span></span>

<span data-ttu-id="09bdb-291">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-291">No</span></span>

<span data-ttu-id="09bdb-292">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-292">Yes</span></span>

<span data-ttu-id="09bdb-293">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-293">No</span></span> 

<span data-ttu-id="09bdb-294">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-294">No</span></span> 

<span data-ttu-id="09bdb-295">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-295">False</span></span>

<span data-ttu-id="09bdb-296">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-296">False</span></span>

<span data-ttu-id="09bdb-297">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-297">Does not appear</span></span>

<span data-ttu-id="09bdb-298">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-298">No</span></span>

<span data-ttu-id="09bdb-299">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-299">No</span></span> 

<span data-ttu-id="09bdb-300">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-300">No</span></span> 

<span data-ttu-id="09bdb-301">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-301">Yes</span></span>

<span data-ttu-id="09bdb-302">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-302">True</span></span>

<span data-ttu-id="09bdb-303">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-303">True</span></span>

<span data-ttu-id="09bdb-304">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-304">Does not appear</span></span>

<span data-ttu-id="09bdb-305">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-305">No</span></span> 

<span data-ttu-id="09bdb-306">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-306">No</span></span> 

<span data-ttu-id="09bdb-307">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-307">No</span></span> 

<span data-ttu-id="09bdb-308">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-308">Yes</span></span>

<span data-ttu-id="09bdb-309">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-309">True</span></span>

<span data-ttu-id="09bdb-310">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-310">False</span></span>

<span data-ttu-id="09bdb-311">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-311">Does not appear</span></span>

<span data-ttu-id="09bdb-312">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-312">No</span></span>

<span data-ttu-id="09bdb-313">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-313">No</span></span> 

<span data-ttu-id="09bdb-314">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-314">No</span></span> 

<span data-ttu-id="09bdb-315">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-315">Yes</span></span>

<span data-ttu-id="09bdb-316">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-316">False</span></span>

<span data-ttu-id="09bdb-317">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-317">True</span></span>

<span data-ttu-id="09bdb-318">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-318">Does not appear</span></span>

<span data-ttu-id="09bdb-319">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-319">No</span></span> 

<span data-ttu-id="09bdb-320">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-320">No</span></span> 

<span data-ttu-id="09bdb-321">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-321">No</span></span> 

<span data-ttu-id="09bdb-322">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-322">Yes</span></span>

<span data-ttu-id="09bdb-323">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-323">False</span></span>

<span data-ttu-id="09bdb-324">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-324">False</span></span>

<span data-ttu-id="09bdb-325">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-325">Does not appear</span></span>

<span data-ttu-id="09bdb-326">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-326">No</span></span>

<span data-ttu-id="09bdb-327">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-327">No</span></span> 

<span data-ttu-id="09bdb-328">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-328">No</span></span> 

<span data-ttu-id="09bdb-329">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-329">No</span></span> 

<span data-ttu-id="09bdb-330">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-330">True</span></span>

<span data-ttu-id="09bdb-331">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-331">True</span></span>

<span data-ttu-id="09bdb-332">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-332">Does not appear</span></span>

<span data-ttu-id="09bdb-333">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-333">No</span></span>

<span data-ttu-id="09bdb-334">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-334">No</span></span> 

<span data-ttu-id="09bdb-335">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-335">No</span></span> 

<span data-ttu-id="09bdb-336">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-336">No</span></span> 

<span data-ttu-id="09bdb-337">是</span><span class="sxs-lookup"><span data-stu-id="09bdb-337">True</span></span>

<span data-ttu-id="09bdb-338">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-338">False</span></span>

<span data-ttu-id="09bdb-339">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-339">Does not appear</span></span>

<span data-ttu-id="09bdb-340">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-340">No</span></span>

<span data-ttu-id="09bdb-341">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-341">No</span></span> 

<span data-ttu-id="09bdb-342">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-342">No</span></span> 

<span data-ttu-id="09bdb-343">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-343">No</span></span> 

<span data-ttu-id="09bdb-344">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-344">False</span></span>

<span data-ttu-id="09bdb-345">True</span><span class="sxs-lookup"><span data-stu-id="09bdb-345">True</span></span>

<span data-ttu-id="09bdb-346">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-346">Does not appear</span></span>

<span data-ttu-id="09bdb-347">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-347">No</span></span>

<span data-ttu-id="09bdb-348">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-348">No</span></span> 

<span data-ttu-id="09bdb-349">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-349">No</span></span> 

<span data-ttu-id="09bdb-350">否</span><span class="sxs-lookup"><span data-stu-id="09bdb-350">No</span></span> 

<span data-ttu-id="09bdb-351">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-351">False</span></span>

<span data-ttu-id="09bdb-352">False</span><span class="sxs-lookup"><span data-stu-id="09bdb-352">False</span></span>

<span data-ttu-id="09bdb-353">未出現</span><span class="sxs-lookup"><span data-stu-id="09bdb-353">Does not appear</span></span>

<span data-ttu-id="09bdb-354">No</span><span class="sxs-lookup"><span data-stu-id="09bdb-354">No</span></span>

 <span data-ttu-id="09bdb-355">如果屬性設定為 null。</span><span class="sxs-lookup"><span data-stu-id="09bdb-355">If the property setting is null.</span></span> <span data-ttu-id="09bdb-356">在某些程式設計語言中，空字串可能不會被解釋為 null 字串。</span><span class="sxs-lookup"><span data-stu-id="09bdb-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="09bdb-357">此命令仍然可以語音存取。</span><span class="sxs-lookup"><span data-stu-id="09bdb-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="09bdb-358">當伺服器收到其中一個命令的輸入時，它會傳送 [**命令**](/windows/desktop/lwef/the-command-object) 事件，並將 **命令** 的名稱傳回做為 [**userinput>**](/windows/desktop/lwef/iagentuserinput) 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="09bdb-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="09bdb-359">然後，您可以使用條件陳述式來比對和處理 **命令**。</span><span class="sxs-lookup"><span data-stu-id="09bdb-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

