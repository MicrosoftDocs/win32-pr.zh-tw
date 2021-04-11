---
title: 建立範例專案
description: 建立範例專案
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player 線上商店，建立範例專案
- 線上商店，建立範例專案
- 輸入2個線上商店，建立範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- 外掛程式，專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 建立範例專案
- 範例，請輸入2個線上商店
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104092574"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="a50ed-117">建立範例專案</span><span class="sxs-lookup"><span data-stu-id="a50ed-117">Creating a Sample Project</span></span>

<span data-ttu-id="a50ed-118">若要使用專案嚮導建立新的專案，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a50ed-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="a50ed-119">開啟 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="a50ed-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="a50ed-120">從 [檔案] 功能表，指向 [新增]，然後按一下 [專案]。</span><span class="sxs-lookup"><span data-stu-id="a50ed-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="a50ed-121">在 [ **專案類型** ] 清單方塊中，選擇 [ **Visual C++ 專案**]。</span><span class="sxs-lookup"><span data-stu-id="a50ed-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="a50ed-122">在 [ **範本** ] 清單方塊中，選擇 Windows Media Player 的 [ **線上商店] Wizard**。</span><span class="sxs-lookup"><span data-stu-id="a50ed-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="a50ed-123">輸入專案的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="a50ed-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="a50ed-124">按一下 **[確定** ] 以啟動專案嚮導。</span><span class="sxs-lookup"><span data-stu-id="a50ed-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="a50ed-125">選取 [ **類型 2] (基本整合)**，然後按 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="a50ed-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="a50ed-126">輸入服務的易記名稱和內容散發者識別碼。</span><span class="sxs-lookup"><span data-stu-id="a50ed-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="a50ed-127">輸入從使用者電腦移除服務之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="a50ed-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="a50ed-128">您為內容散發者識別碼提供的值不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="a50ed-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="a50ed-129">Wizard 會從您提供的字串中移除任何空格。</span><span class="sxs-lookup"><span data-stu-id="a50ed-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="a50ed-130">按一下 [完成] 以建立專案。</span><span class="sxs-lookup"><span data-stu-id="a50ed-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="a50ed-131">Wizard 會自動產生新的 c + + 專案，以建立可執行 **IWMPSubscriptionService** 和 **IWMPSubscriptionService2** 介面的 type 2 online store 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="a50ed-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="a50ed-132">您每次執行嚮導時，都會建立相同的專案，但當您編譯專案時所建立的元件會有唯一的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a50ed-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="a50ed-133">根據您在執行嚮導時所提供的值，專案名稱、易記名稱和內容散發者識別碼也可能不同。</span><span class="sxs-lookup"><span data-stu-id="a50ed-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="a50ed-134">範例專案會使用符合您為易記名稱提供之值的索引鍵名稱來註冊元件。</span><span class="sxs-lookup"><span data-stu-id="a50ed-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="a50ed-135">此範例會使用 Active Template Library (ATL) 程式碼來提供 COM 執行。</span><span class="sxs-lookup"><span data-stu-id="a50ed-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="a50ed-136">嚮導會為您建立下列檔案：</span><span class="sxs-lookup"><span data-stu-id="a50ed-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="a50ed-137">*專案名稱* dll .cpp。</span><span class="sxs-lookup"><span data-stu-id="a50ed-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="a50ed-138">將動態連結程式庫 (DLL) 匯出，例如主要 DLL 進入點函數。</span><span class="sxs-lookup"><span data-stu-id="a50ed-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="a50ed-139">也包含 ATL 物件對應和模組宣告。</span><span class="sxs-lookup"><span data-stu-id="a50ed-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="a50ed-140">*專案名稱*.cpp。</span><span class="sxs-lookup"><span data-stu-id="a50ed-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="a50ed-141">包含 IWMPSubscriptionService 和 IWMPSubscriptionService2 介面之方法的預設實值。</span><span class="sxs-lookup"><span data-stu-id="a50ed-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="a50ed-142">也包含程式碼，用來定義當 Windows Media Player 呼叫方法時，範例會開啟的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a50ed-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="a50ed-143">*專案名稱*.def。宣告 DLL 匯出。</span><span class="sxs-lookup"><span data-stu-id="a50ed-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="a50ed-144">Stdafx.h .cpp。</span><span class="sxs-lookup"><span data-stu-id="a50ed-144">StdAfx.cpp.</span></span> <span data-ttu-id="a50ed-145">包含標準標頭。</span><span class="sxs-lookup"><span data-stu-id="a50ed-145">Includes standard headers.</span></span>
-   <span data-ttu-id="a50ed-146">wmp. h。</span><span class="sxs-lookup"><span data-stu-id="a50ed-146">wmp.h.</span></span> <span data-ttu-id="a50ed-147">Windows Media Player 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a50ed-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="a50ed-148">wmpplug。</span><span class="sxs-lookup"><span data-stu-id="a50ed-148">wmpplug.h.</span></span> <span data-ttu-id="a50ed-149">Windows Media Player 外掛程式標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a50ed-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="a50ed-150">subscriptionservices。</span><span class="sxs-lookup"><span data-stu-id="a50ed-150">subscriptionservices.h.</span></span> <span data-ttu-id="a50ed-151">Windows Media Player online 會儲存標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a50ed-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="a50ed-152">資源 .h。</span><span class="sxs-lookup"><span data-stu-id="a50ed-152">resource.h.</span></span> <span data-ttu-id="a50ed-153">包含資源定義。</span><span class="sxs-lookup"><span data-stu-id="a50ed-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="a50ed-154">**專案名稱**.h。</span><span class="sxs-lookup"><span data-stu-id="a50ed-154">**ProjectName**.h.</span></span> <span data-ttu-id="a50ed-155">包含線上商店物件和對話方塊的類別定義。</span><span class="sxs-lookup"><span data-stu-id="a50ed-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="a50ed-156">定義物件的類別識別碼和內容散發者識別碼常數。</span><span class="sxs-lookup"><span data-stu-id="a50ed-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="a50ed-157">Stdafx.h。</span><span class="sxs-lookup"><span data-stu-id="a50ed-157">StdAfx.h.</span></span> <span data-ttu-id="a50ed-158">包含標準系統包含。</span><span class="sxs-lookup"><span data-stu-id="a50ed-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="a50ed-159">*專案名稱*。</span><span class="sxs-lookup"><span data-stu-id="a50ed-159">*ProjectName*.rc.</span></span> <span data-ttu-id="a50ed-160">資源腳本檔。</span><span class="sxs-lookup"><span data-stu-id="a50ed-160">The resource script file.</span></span> <span data-ttu-id="a50ed-161">這包含對話方塊資源和控制項的定義。</span><span class="sxs-lookup"><span data-stu-id="a50ed-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="a50ed-162">這也是字串資料表的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="a50ed-162">This is also where the string table is stored.</span></span> <span data-ttu-id="a50ed-163">字串資料表包含您的專案名稱和易記名稱的字串常數。</span><span class="sxs-lookup"><span data-stu-id="a50ed-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="a50ed-164">通常您會使用 Visual Studio 資源編輯器中的這個檔案，而不是純文字。</span><span class="sxs-lookup"><span data-stu-id="a50ed-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="a50ed-165">*專案名稱*.rgs。</span><span class="sxs-lookup"><span data-stu-id="a50ed-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="a50ed-166">登入指令檔檔。</span><span class="sxs-lookup"><span data-stu-id="a50ed-166">The registry script file.</span></span> <span data-ttu-id="a50ed-167">此檔案包含用來將您的元件類別新增至登錄的資訊，讓 Windows Media Player 可以找到它。</span><span class="sxs-lookup"><span data-stu-id="a50ed-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="a50ed-168">您可以在此檔案中變更服務的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="a50ed-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="a50ed-169">您應該將 DLL 的基底位址設定為0x0F100000，以避免與 Windows Media Player 衝突。</span><span class="sxs-lookup"><span data-stu-id="a50ed-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a50ed-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="a50ed-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50ed-171">**建立 Type 2 線上商店的外掛程式**</span><span class="sxs-lookup"><span data-stu-id="a50ed-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a50ed-172">**IWMPSubscriptionService 介面**</span><span class="sxs-lookup"><span data-stu-id="a50ed-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="a50ed-173">**IWMPSubscriptionService2 介面**</span><span class="sxs-lookup"><span data-stu-id="a50ed-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




