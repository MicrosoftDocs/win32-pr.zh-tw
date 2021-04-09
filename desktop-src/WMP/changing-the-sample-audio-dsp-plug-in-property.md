---
title: 變更範例音訊 DSP 外掛程式屬性
description: 變更範例音訊 DSP 外掛程式屬性
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊屬性
- DSP 外掛程式、音訊屬性
- 音訊 DSP 外掛程式，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674323"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="0f8d0-108">變更範例音訊 DSP 外掛程式屬性</span><span class="sxs-lookup"><span data-stu-id="0f8d0-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="0f8d0-109">您可能會想要變更 Windows Media Player 外掛程式 Wizard 預設建立的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="0f8d0-110">下列清單詳細說明可能需要變更的專案：</span><span class="sxs-lookup"><span data-stu-id="0f8d0-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="0f8d0-111">**對話方塊資源。**</span><span class="sxs-lookup"><span data-stu-id="0f8d0-111">**The dialog resource.**</span></span> <span data-ttu-id="0f8d0-112">按一下 [專案工作區] 視窗中的 [ **ResourceView** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="0f8d0-113">展開資料夾清單以開啟對話方塊資料夾。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="0f8d0-114">按兩下對話方塊資源以開啟資源編輯器。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="0f8d0-115">您可以對 [屬性頁] 對話方塊進行變更，以滿足您的需求。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="0f8d0-116">例如，您可以變更標籤中的文字，或以核取方塊取代編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="0f8d0-117">**屬性頁物件程式碼。**</span><span class="sxs-lookup"><span data-stu-id="0f8d0-117">**The property page object code.**</span></span> <span data-ttu-id="0f8d0-118">預設的執行會使用類型為 double 的變數來儲存比例因數。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="0f8d0-119">您可能需要不同類型的資料。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-119">You might require a different type of data.</span></span> <span data-ttu-id="0f8d0-120">這也需要您變更將資料保存到登錄的程式碼，並從登錄中讀取資料 (包括從 *CProjectName*：：**FinalConstruct**) 中的登錄讀取的程式碼。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="0f8d0-121">**儲存屬性值的成員變數。**</span><span class="sxs-lookup"><span data-stu-id="0f8d0-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="0f8d0-122">此變數命名為 "m \_ fScaleFactor"，並宣告為 double 類型。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="0f8d0-123">您可能會想要在整個專案中變更這個變數的名稱和類型。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="0f8d0-124">**屬性 get 和屬性 put 方法。**</span><span class="sxs-lookup"><span data-stu-id="0f8d0-124">**The property get and property put methods.**</span></span> <span data-ttu-id="0f8d0-125">您可能會想要變更這些方法的名稱、參數和執行方式。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="0f8d0-126">別忘了也在專案中的其他地方反映這些變更。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="0f8d0-127">例如， **屬性頁會** 套用方法呼叫 *CProjectName*：：**put \_ 小** 數位數。</span><span class="sxs-lookup"><span data-stu-id="0f8d0-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f8d0-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f8d0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f8d0-129">**執行音訊 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="0f8d0-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




