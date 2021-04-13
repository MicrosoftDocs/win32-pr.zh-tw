---
title: 修改 Echo 對話資源
description: 修改 Echo 對話資源
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，對話方塊資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301483"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="0e979-109">修改 Echo 對話資源</span><span class="sxs-lookup"><span data-stu-id="0e979-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="0e979-110">您需要變更對話方塊資源，也就是屬性頁物件的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0e979-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="0e979-111">您可以先變更現有的編輯方塊和標籤，使其適用于 [延遲時間] 屬性，然後為 [潮濕混合] 屬性新增第二個編輯方塊和標籤。</span><span class="sxs-lookup"><span data-stu-id="0e979-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="0e979-112">若要在 Visual C++ 中編輯對話方塊資源：</span><span class="sxs-lookup"><span data-stu-id="0e979-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="0e979-113">按一下 [專案] 工作區中的 [ **ResourceView** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0e979-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="0e979-114">開啟最上層資料夾，展開 [資源] 樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="0e979-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="0e979-115">開啟 **對話方塊** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="0e979-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="0e979-116">按兩下對話方塊資源名稱 [IDD \_ ECHOPROPPAGE]。</span><span class="sxs-lookup"><span data-stu-id="0e979-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="0e979-117">資源編輯器會出現在右窗格中。</span><span class="sxs-lookup"><span data-stu-id="0e979-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="0e979-118">變更現有的資源</span><span class="sxs-lookup"><span data-stu-id="0e979-118">Changing the Existing Resources</span></span>

<span data-ttu-id="0e979-119">若要變更延遲時間屬性的現有屬性頁資源：</span><span class="sxs-lookup"><span data-stu-id="0e979-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="0e979-120">首先，變更現有靜態文字控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="0e979-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="0e979-121">以滑鼠右鍵按一下控制項，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="0e979-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="0e979-122">在 [ **標題** ] 欄位中，輸入新的標題：</span><span class="sxs-lookup"><span data-stu-id="0e979-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="0e979-123">關閉 [文字屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="0e979-124">現在，變更編輯方塊控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e979-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="0e979-125">若要這樣做，請以滑鼠右鍵按一下控制項，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="0e979-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="0e979-126">在 [ **識別碼** ] 欄位中，輸入控制項的新名稱：</span><span class="sxs-lookup"><span data-stu-id="0e979-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="0e979-127">關閉 [編輯屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="0e979-128">儲存資源。</span><span class="sxs-lookup"><span data-stu-id="0e979-128">Save the resource.</span></span>
6.  <span data-ttu-id="0e979-129">如果系統提示您重載檔案資源 .h，請回答 **[是]** 。</span><span class="sxs-lookup"><span data-stu-id="0e979-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="0e979-130">按一下 [專案] 工作區中的 [ **FileView** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0e979-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="0e979-131">開啟資源。h</span><span class="sxs-lookup"><span data-stu-id="0e979-131">Open resource.h</span></span>
8.  <span data-ttu-id="0e979-132">找出 \# (IDC SCALEFACTOR) 的 [縮放比例] 編輯方塊資源的定義 \_ ，並將其刪除。</span><span class="sxs-lookup"><span data-stu-id="0e979-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="0e979-133">它應該具有與 IDC DELAYTIME 相同的識別碼號碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e979-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="0e979-134">加入新的資源</span><span class="sxs-lookup"><span data-stu-id="0e979-134">Adding the New Resources</span></span>

<span data-ttu-id="0e979-135">若要加入新的 [潮濕混合] 屬性的屬性頁資源：</span><span class="sxs-lookup"><span data-stu-id="0e979-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="0e979-136">按一下 [專案] 工作區中的 [ **ResourceView** ] 索引標籤，即可選取它。</span><span class="sxs-lookup"><span data-stu-id="0e979-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="0e979-137">按兩下 [屬性頁] 對話方塊的 [名稱]，然後按一下 [IDD \_ ECHOPROPPAGE]。</span><span class="sxs-lookup"><span data-stu-id="0e979-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="0e979-138">資源編輯器會出現在右窗格中。</span><span class="sxs-lookup"><span data-stu-id="0e979-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="0e979-139">使用 [工具箱] 將靜態文字控制項和編輯方塊加入至屬性頁。</span><span class="sxs-lookup"><span data-stu-id="0e979-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="0e979-140">以滑鼠右鍵按一下靜態文字控制項，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="0e979-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="0e979-141">在 [ **識別碼** ] 欄位中輸入靜態文字控制項的新名稱：</span><span class="sxs-lookup"><span data-stu-id="0e979-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="0e979-142">輸入標籤的標題：</span><span class="sxs-lookup"><span data-stu-id="0e979-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="0e979-143">關閉 [文字屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="0e979-144">以滑鼠右鍵按一下編輯方塊，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="0e979-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="0e979-145">在 [ **識別碼** ] 欄位中輸入編輯方塊的新名稱：</span><span class="sxs-lookup"><span data-stu-id="0e979-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="0e979-146">關閉 [編輯屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="0e979-147">當您儲存專案時，系統可能會提示您重載資源 .h。</span><span class="sxs-lookup"><span data-stu-id="0e979-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="0e979-148">如果發生這種情況，請按一下 **[是]** 。</span><span class="sxs-lookup"><span data-stu-id="0e979-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="0e979-149">對話方塊資源編輯器應該針對您新增的專案，將資源名稱和識別碼加入至 .h。</span><span class="sxs-lookup"><span data-stu-id="0e979-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="0e979-150">如果基於某些原因而不會發生這種情況，您必須開啟 []，並輸入標籤和編輯方塊控制項的新專案，並指派每個唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e979-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="0e979-151">修改和新增字串資源</span><span class="sxs-lookup"><span data-stu-id="0e979-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="0e979-152">外掛程式 wizard 範例程式碼會指定名為 ID SCALERANGEERROR 的字串資源 \_ ，其中包含當使用者輸入超出範圍時要顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="0e979-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="0e979-153">您可以依照 Visual C++ 中的下列步驟，修改此資源以符合您的延遲時間值需求：</span><span class="sxs-lookup"><span data-stu-id="0e979-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="0e979-154">按一下 [ **ResourceView** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0e979-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="0e979-155">開啟 [ **字串資料表** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="0e979-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="0e979-156">按兩下 [ **字串資料表** ] 圖示以開啟 [資源編輯器]。</span><span class="sxs-lookup"><span data-stu-id="0e979-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="0e979-157">按兩下您想要編輯的資源名稱，在此案例中為 [識別碼] \_ SCALERANGEERROR。</span><span class="sxs-lookup"><span data-stu-id="0e979-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="0e979-158">[字串屬性] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="0e979-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="0e979-159">將 [ **識別碼** ] 欄位中的名稱變更為 [識別碼] \_ DELAYRANGEERROR。</span><span class="sxs-lookup"><span data-stu-id="0e979-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="0e979-160">變更 [ **標題** ] 欄位中的文字：</span><span class="sxs-lookup"><span data-stu-id="0e979-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="0e979-161">關閉 [字串屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="0e979-162">接下來，為潮濕混合屬性錯誤訊息新增字串資源。</span><span class="sxs-lookup"><span data-stu-id="0e979-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="0e979-163">按兩下資源編輯器底部的空白行。</span><span class="sxs-lookup"><span data-stu-id="0e979-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="0e979-164">將 [ **識別碼** ] 欄位中的名稱變更為 [識別碼] \_ MIXRANGEERROR。</span><span class="sxs-lookup"><span data-stu-id="0e979-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="0e979-165">在 [ **標題** ] 欄位中加入下列文字：</span><span class="sxs-lookup"><span data-stu-id="0e979-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="0e979-166">關閉 [字串屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e979-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="0e979-167">您會想要在字串資料表中變更其他兩個值。</span><span class="sxs-lookup"><span data-stu-id="0e979-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="0e979-168">識別碼 \_ FRIENDLYNAME 是 Windows Media Player 使用者介面中顯示的名稱，用來識別外掛程式。</span><span class="sxs-lookup"><span data-stu-id="0e979-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="0e979-169">識別碼 \_ 描述可讓您告訴使用者您的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="0e979-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="0e979-170">這兩個字串都會以參數形式傳遞至 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** 函式，該函式是在 Echodll 的 DllRegisterServer 方法中呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e979-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e979-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e979-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e979-172">**修改 Echo 範例屬性頁**</span><span class="sxs-lookup"><span data-stu-id="0e979-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




