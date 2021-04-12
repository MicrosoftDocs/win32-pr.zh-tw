---
title: 按鈕狀態
description: 本節將討論如何選取按鈕來變更其狀態，以及應用程式應該如何回應。
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463809"
---
# <a name="button-states"></a><span data-ttu-id="a5c5c-103">按鈕狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-103">Button States</span></span>

<span data-ttu-id="a5c5c-104">本節將討論如何選取按鈕來變更其狀態，以及應用程式應該如何回應。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-104">This section discusses how selecting a button changes its state and how the application should respond.</span></span>

<span data-ttu-id="a5c5c-105">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="a5c5c-105">The section consists of the following topics:</span></span>

-   [<span data-ttu-id="a5c5c-106">按鈕選取</span><span class="sxs-lookup"><span data-stu-id="a5c5c-106">Button Selection</span></span>](#button-selection)
-   [<span data-ttu-id="a5c5c-107">按鈕狀態的元素</span><span class="sxs-lookup"><span data-stu-id="a5c5c-107">Elements of a Button State</span></span>](#elements-of-a-button-state)
    -   [<span data-ttu-id="a5c5c-108">焦點狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-108">Focus State</span></span>](#focus-state)
    -   [<span data-ttu-id="a5c5c-109">推送狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-109">Push State</span></span>](#push-state)
    -   [<span data-ttu-id="a5c5c-110">檢查狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-110">Check State</span></span>](#check-state)
-   [<span data-ttu-id="a5c5c-111">按鈕狀態的變更</span><span class="sxs-lookup"><span data-stu-id="a5c5c-111">Changes to a Button State</span></span>](#changes-to-a-button-state)

## <a name="button-selection"></a><span data-ttu-id="a5c5c-112">按鈕選取</span><span class="sxs-lookup"><span data-stu-id="a5c5c-112">Button Selection</span></span>

<span data-ttu-id="a5c5c-113">使用者可以透過下列三種方式來選取按鈕：以滑鼠按一下按鈕、依序移至該按鈕，然後按下 ENTER 鍵，或者 (如果按鈕是 [**WS \_ group**](/windows/desktop/winmsg/window-styles) 樣式所定義之群組的一部分) 方法是在群組中使用方向鍵，然後使用方向鍵在該群組內移動。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-113">The user can select a button in three ways: by clicking it with the mouse, by tabbing to it and then pressing the ENTER key, or (if the button is part of a group defined by the [**WS\_GROUP**](/windows/desktop/winmsg/window-styles) style) by tabbing to the selected button in the group and using the arrow keys to move within that group.</span></span> <span data-ttu-id="a5c5c-114">這兩個定位方法是系統所提供的預先定義鍵盤介面的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-114">The two tabbing methods are part of the predefined keyboard interface provided by the system.</span></span> <span data-ttu-id="a5c5c-115">如需此介面的完整描述，請參閱 [對話方塊](/windows/desktop/dlgbox/dialog-boxes)。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-115">For a complete description of this interface, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

<span data-ttu-id="a5c5c-116">選取按鈕通常會導致下列事件：</span><span class="sxs-lookup"><span data-stu-id="a5c5c-116">Selecting a button typically causes the following events:</span></span>

-   <span data-ttu-id="a5c5c-117">系統會為按鈕提供鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-117">The system gives the button the keyboard focus.</span></span>
-   <span data-ttu-id="a5c5c-118">按鈕會將訊息傳送給其父視窗，以通知其選取專案。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-118">The button sends its parent window a message to notify it of the selection.</span></span>
-   <span data-ttu-id="a5c5c-119">父視窗 (或系統) 傳送訊息給按鈕以變更其狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-119">The parent window (or the system) sends the button a message to change its state.</span></span>
-   <span data-ttu-id="a5c5c-120">父視窗 (或系統) 會重新繪製按鈕，以反映其新狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-120">The parent window (or the system) repaints the button to reflect its new state.</span></span>

## <a name="elements-of-a-button-state"></a><span data-ttu-id="a5c5c-121">按鈕狀態的元素</span><span class="sxs-lookup"><span data-stu-id="a5c5c-121">Elements of a Button State</span></span>

<span data-ttu-id="a5c5c-122">按鈕的狀態可依焦點狀態、推播狀態和檢查狀態來表徵。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-122">A button's state can be characterized by its focus state, push state, and check state.</span></span>

-   [<span data-ttu-id="a5c5c-123">焦點狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-123">Focus State</span></span>](#focus-state)
-   [<span data-ttu-id="a5c5c-124">推送狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-124">Push State</span></span>](#push-state)
-   [<span data-ttu-id="a5c5c-125">檢查狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-125">Check State</span></span>](#check-state)

### <a name="focus-state"></a><span data-ttu-id="a5c5c-126">焦點狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-126">Focus State</span></span>

<span data-ttu-id="a5c5c-127">焦點狀態適用于核取方塊、選項按鈕、推播按鈕或主控描繪按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-127">The focus state applies to a check box, radio button, push button, or owner-drawn button.</span></span> <span data-ttu-id="a5c5c-128">當使用者選取按鈕時，按鈕就會收到鍵盤焦點，並在使用者選取另一個控制項時失去焦點。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-128">A button receives the keyboard focus when the user selects it and loses the focus when the user selects another control.</span></span> <span data-ttu-id="a5c5c-129">一次只能有一個控制項可以有鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-129">Only one control can have the keyboard focus at a time.</span></span>

<span data-ttu-id="a5c5c-130">當按鈕具有鍵盤焦點時，系統通常會以虛線括住，以反白顯示按鈕的文字、圖示或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-130">When a button has the keyboard focus, the system typically highlights the text, icon, or bitmap of a button by surrounding it with a dotted line.</span></span> <span data-ttu-id="a5c5c-131">此外，當按鈕具有焦點時，按鈕的深色框線也會很高。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-131">In addition, a push button has a heavy dark border when it has the focus.</span></span> <span data-ttu-id="a5c5c-132">系統會自動變更自動按鈕的醒目提示，但應用程式必須藉由傳送訊息來變更非自動按鈕的醒目提示。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-132">The system automatically changes the highlight for an automatic button, but the application must change the highlight for a non-automatic button by sending messages.</span></span>

### <a name="push-state"></a><span data-ttu-id="a5c5c-133">推送狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-133">Push State</span></span>

<span data-ttu-id="a5c5c-134">推送狀態會套用至下拉按鈕、核取方塊、選項按鈕或三個狀態的核取方塊，但不適用於其他按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-134">The push state applies to a push button, check box, radio button, or three-state check box, but does not apply to other buttons.</span></span> <span data-ttu-id="a5c5c-135">按鈕的推送狀態可以是已推送或未推送。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-135">The push state of a button can be either pushed or not pushed.</span></span> <span data-ttu-id="a5c5c-136">推送按鈕 (或具有 [**BS \_ PUSHLIKE**](button-styles.md) 樣式) 的任何按鈕時，按鈕就會繪製為凹陷按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-136">When a push button (or any button with the [**BS\_PUSHLIKE**](button-styles.md) style) is pushed, the button is drawn as a sunken button.</span></span> <span data-ttu-id="a5c5c-137">未推送時，會將它繪製為引發按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-137">When it is not pushed, it is drawn as a raised button.</span></span> <span data-ttu-id="a5c5c-138">按一下核取方塊、選項按鈕或三個狀態核取方塊時，按鈕的背景會呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-138">When a check box, radio button, or three-state check box is clicked, the background of the button is grayed.</span></span> <span data-ttu-id="a5c5c-139">未推送時，按鈕的背景不會呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-139">When it is not pushed, the background of the button is not grayed.</span></span>

### <a name="check-state"></a><span data-ttu-id="a5c5c-140">檢查狀態</span><span class="sxs-lookup"><span data-stu-id="a5c5c-140">Check State</span></span>

<span data-ttu-id="a5c5c-141">檢查狀態適用于核取方塊、選項按鈕或三個狀態核取方塊，但不適用於其他按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-141">The check state applies to a check box, radio button, or three-state check box, but does not apply to other buttons.</span></span> <span data-ttu-id="a5c5c-142">您可以針對三種狀態的核取方塊檢查、清除或 (狀態，) 不定。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-142">The state can be checked, cleared, or (for three-state check boxes) indeterminate.</span></span> <span data-ttu-id="a5c5c-143">如果核取方塊包含核取記號，則會核取該核取方塊，並在沒有核取方塊時清除。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-143">A check box is checked when it contains a check mark, and is cleared when it does not.</span></span> <span data-ttu-id="a5c5c-144">當選項按鈕包含黑色點時，就會核取該按鈕;當它不存在時，就會清除此選項。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-144">A radio button is checked when it contains a black dot; it is cleared when it does not.</span></span> <span data-ttu-id="a5c5c-145">如果有三個狀態核取方塊，則會在它包含核取記號時加以清除，如果沒有，則會清除，而且當它包含灰色方塊時，則會予以不定。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-145">A three-state check box is checked when it contains a check mark, is cleared when it does not, and is indeterminate when it contains a grayed box.</span></span> <span data-ttu-id="a5c5c-146">系統會自動變更自動按鈕的檢查狀態，但應用程式必須變更非自動按鈕的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-146">The system automatically changes the check state of an automatic button, but the application must change the check state of a non-automatic button.</span></span>

## <a name="changes-to-a-button-state"></a><span data-ttu-id="a5c5c-147">按鈕狀態的變更</span><span class="sxs-lookup"><span data-stu-id="a5c5c-147">Changes to a Button State</span></span>

<span data-ttu-id="a5c5c-148">當使用者選取按鈕時，通常需要變更一或多個按鈕的狀態元素。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-148">When the user selects a button, it is generally necessary to change one or more of the button's state elements.</span></span> <span data-ttu-id="a5c5c-149">系統會自動變更所有按鈕類型的焦點狀態、推播按鈕的推送狀態或具有 [**BS \_ PUSHLIKE**](button-styles.md) 樣式的按鈕，以及所有自動按鈕的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-149">The system automatically changes the focus state for all button types, the push state for push buttons or buttons with the [**BS\_PUSHLIKE**](button-styles.md) style, and the check state for all automatic buttons.</span></span> <span data-ttu-id="a5c5c-150">應用程式必須進行所有其他狀態變更，並將按鈕的類型、樣式和目前的狀態納入考慮。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-150">The application must make all other state changes, taking into account the button's type, style, and current state.</span></span> <span data-ttu-id="a5c5c-151">下列清單顯示每個按鈕類型必須變更的狀態元素：</span><span class="sxs-lookup"><span data-stu-id="a5c5c-151">The following list shows the state elements that must be changed for each button type:</span></span>

-   <span data-ttu-id="a5c5c-152">核取方塊必須變更檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-152">A check box must change the check state.</span></span>
-   <span data-ttu-id="a5c5c-153">選項按鈕必須變更檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-153">A radio button must change the check state.</span></span> <span data-ttu-id="a5c5c-154">您也可能需要變更相同群組中其他選項按鈕的檢查狀態，以確保選項按鈕的互斥本質。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-154">It may also be necessary to change the check state of other radio buttons in the same group to ensure the mutually exclusive nature of radio buttons.</span></span>
-   <span data-ttu-id="a5c5c-155">由於主控描繪按鈕的狀態與應用程式相依，因此應用程式在按鈕中必須變更的內容可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-155">Because the state of an owner-drawn button is application dependent, what the application must change in the button can vary.</span></span> <span data-ttu-id="a5c5c-156">必須變更群組方塊的元素，因為使用者無法選取群組框。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-156">No elements of a group box must be changed, because users cannot select group boxes.</span></span>

<span data-ttu-id="a5c5c-157">應用程式可以將 [**BM \_ GETCHECK**](bm-getcheck.md) 或 [**BM \_ >getstate**](bm-getstate.md) 訊息傳送給它，藉以判斷按鈕的狀態; 應用程式可以將 [**BM \_ SETCHECK**](bm-setcheck.md) 或 [**BM \_ SETSTATE**](bm-setstate.md) 訊息傳送給它，藉以設定按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c5c-157">An application can determine a button's state by sending it a [**BM\_GETCHECK**](bm-getcheck.md) or [**BM\_GETSTATE**](bm-getstate.md) message; the application can set a button's state by sending it a [**BM\_SETCHECK**](bm-setcheck.md) or [**BM\_SETSTATE**](bm-setstate.md) message.</span></span>

 

 