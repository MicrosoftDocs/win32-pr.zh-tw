---
title: CONTROL 控制項
description: 定義使用者定義控制項。
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- 控制控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933171"
---
# <a name="control-control"></a><span data-ttu-id="adfff-104">CONTROL 控制項</span><span class="sxs-lookup"><span data-stu-id="adfff-104">CONTROL control</span></span>

<span data-ttu-id="adfff-105">定義使用者定義控制項。</span><span class="sxs-lookup"><span data-stu-id="adfff-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="adfff-106"><span id="class"></span><span id="CLASS"></span>*類*</span><span class="sxs-lookup"><span data-stu-id="adfff-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="adfff-107">定義類別的名稱、字元字串或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="adfff-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="adfff-108">這可以是任何一個控制項類別，如需控制項類別的清單，請參閱此描述後面的第一個清單。</span><span class="sxs-lookup"><span data-stu-id="adfff-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="adfff-109">如果值是應用程式所提供的重新定義名稱，則必須是以雙引號括住的字串 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="adfff-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="adfff-110"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="adfff-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="adfff-111">重新定義的名稱或整數值，可指定指定控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="adfff-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="adfff-112">*樣式* 的確切意義取決於 *類別* 值。</span><span class="sxs-lookup"><span data-stu-id="adfff-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="adfff-113">此描述後面的各節會顯示控制項類別和對應的樣式。</span><span class="sxs-lookup"><span data-stu-id="adfff-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="adfff-114">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adfff-115">備註</span><span class="sxs-lookup"><span data-stu-id="adfff-115">Remarks</span></span>

<span data-ttu-id="adfff-116">下列各節將說明六個可能的控制項類別。</span><span class="sxs-lookup"><span data-stu-id="adfff-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="adfff-117">Button 控制項類別</span><span class="sxs-lookup"><span data-stu-id="adfff-117">The Button Control Class</span></span>

<span data-ttu-id="adfff-118">按鈕控制項是一個小型的矩形子視窗，使用者可以按一下滑鼠將其開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="adfff-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="adfff-119">按鈕控制項可以單獨使用，也可以在群組中使用，也可以在不使用文字的情況下標記或顯示。</span><span class="sxs-lookup"><span data-stu-id="adfff-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="adfff-120">按鈕控制項通常會在使用者按一下時變更外觀。</span><span class="sxs-lookup"><span data-stu-id="adfff-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="adfff-121">按鈕樣式將在下列主題中說明： [按鈕樣式](../controls/button-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="adfff-122">下拉式方塊控制項類別</span><span class="sxs-lookup"><span data-stu-id="adfff-122">The Combo Box Control Class</span></span>

<span data-ttu-id="adfff-123">下拉式方塊控制項包含選項欄位，類似于編輯控制項加上清單方塊。</span><span class="sxs-lookup"><span data-stu-id="adfff-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="adfff-124">清單方塊可能會隨時顯示，或在使用者選取 [選取範圍] 欄位旁的 [彈出方塊] 時下降。</span><span class="sxs-lookup"><span data-stu-id="adfff-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="adfff-125">根據下拉式方塊的樣式，使用者可以或無法編輯選取欄位的內容。</span><span class="sxs-lookup"><span data-stu-id="adfff-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="adfff-126">如果看不到清單方塊，請在選取方塊中輸入字元，將會導致符合輸入之字元的第一個專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="adfff-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="adfff-127">相反地，在清單方塊中選取專案時，會在 [選取範圍] 欄位中顯示選取的文字。</span><span class="sxs-lookup"><span data-stu-id="adfff-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="adfff-128">下列主題將說明下拉式方塊控制項樣式： [下拉式方塊樣式](../controls/combo-box-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="adfff-129">編輯控制項類別</span><span class="sxs-lookup"><span data-stu-id="adfff-129">The Edit Control Class</span></span>

<span data-ttu-id="adfff-130">編輯控制項是一個矩形子視窗，使用者可以在其中輸入鍵盤中的文字。</span><span class="sxs-lookup"><span data-stu-id="adfff-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="adfff-131">使用者選取控制項，並為其提供輸入焦點，方法是按一下其中的滑鼠，或按下 TAB 鍵。</span><span class="sxs-lookup"><span data-stu-id="adfff-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="adfff-132">當控制項顯示閃爍的插入點時，使用者可以輸入文字。</span><span class="sxs-lookup"><span data-stu-id="adfff-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="adfff-133">您可以使用滑鼠來移動游標並選取要取代的字元，或將游標置於插入字元的位置。</span><span class="sxs-lookup"><span data-stu-id="adfff-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="adfff-134">倒退鍵可以用來刪除字元。</span><span class="sxs-lookup"><span data-stu-id="adfff-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="adfff-135">編輯控制項使用固定音調字型，並顯示 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="adfff-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="adfff-136">它們會將 tab 字元展開為將游標移至下一個索引標籤時所需的空白字元數。</span><span class="sxs-lookup"><span data-stu-id="adfff-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="adfff-137">Tab 鍵會假設為每8個字元的位置。</span><span class="sxs-lookup"><span data-stu-id="adfff-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="adfff-138">下列主題描述編輯控制項樣式： [編輯控制項樣式](../controls/edit-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="adfff-139">清單方塊控制項類別</span><span class="sxs-lookup"><span data-stu-id="adfff-139">The List Box Control Class</span></span>

<span data-ttu-id="adfff-140">清單方塊控制項是由字元字串清單所組成。</span><span class="sxs-lookup"><span data-stu-id="adfff-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="adfff-141">每當應用程式需要顯示使用者可查看和選取的名稱清單（例如檔案名）時，就會使用此控制項。</span><span class="sxs-lookup"><span data-stu-id="adfff-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="adfff-142">使用者可以選取字串，方法是使用滑鼠指向字串，然後按一下滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="adfff-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="adfff-143">選取字串時，會將它反白顯示，並將通知訊息傳遞至父視窗。</span><span class="sxs-lookup"><span data-stu-id="adfff-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="adfff-144">捲軸可以與清單方塊控制項搭配使用，以滾動對控制項視窗而言太長或太寬的清單。</span><span class="sxs-lookup"><span data-stu-id="adfff-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="adfff-145">下列主題將描述清單方塊控制項樣式： [清單方塊樣式](../controls/list-box-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="adfff-146">Scroll-Bar Control 類別</span><span class="sxs-lookup"><span data-stu-id="adfff-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="adfff-147">捲軸控制項是包含捲動方塊的矩形，而且兩端都有方向箭號。</span><span class="sxs-lookup"><span data-stu-id="adfff-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="adfff-148">每當使用者按一下控制項中的滑鼠時，捲軸就會將通知訊息傳送至其父代。</span><span class="sxs-lookup"><span data-stu-id="adfff-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="adfff-149">如有必要，父系負責更新 thumb 位置。</span><span class="sxs-lookup"><span data-stu-id="adfff-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="adfff-150">捲軸控制項的外觀和功能，與一般視窗中使用的捲軸相同。</span><span class="sxs-lookup"><span data-stu-id="adfff-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="adfff-151">但不同于捲軸，捲軸控制項可以放在視窗內的任何位置，並在需要時使用，以提供視窗的滾動輸入。</span><span class="sxs-lookup"><span data-stu-id="adfff-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="adfff-152">捲軸樣式將在下列主題中說明： [捲軸控制項樣式](../controls/scroll-bar-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="adfff-153">靜態控制項類別</span><span class="sxs-lookup"><span data-stu-id="adfff-153">The Static Control Class</span></span>

<span data-ttu-id="adfff-154">靜態控制項是可用於標記、方塊或分隔其他控制項的簡單文字欄位、方塊和矩形。</span><span class="sxs-lookup"><span data-stu-id="adfff-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="adfff-155">靜態控制項不需要輸入，也不提供輸出。</span><span class="sxs-lookup"><span data-stu-id="adfff-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="adfff-156">下列主題描述靜態控制項樣式： [靜態控制項樣式](../controls/static-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="adfff-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 