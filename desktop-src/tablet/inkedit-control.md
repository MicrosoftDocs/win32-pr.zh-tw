---
description: InkEdit 控制項提供簡單的方式來捕捉、辨識和顯示筆墨。
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850023"
---
# <a name="inkedit-control"></a><span data-ttu-id="dd0ac-103">InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="dd0ac-103">InkEdit Control</span></span>

<span data-ttu-id="dd0ac-104">[InkEdit](inkedit-control-reference.md)控制項提供簡單的方式來捕捉、辨識和顯示筆墨。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="dd0ac-105">這種 [InkEdit](inkedit-control-reference.md) 控制項的執行是以 [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) 控制項為基礎。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="dd0ac-106">Managed ( .NET Framework) 的 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 執行是以 [**RichTextBox**](/previous-versions/windows/) 控制項為基礎。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="dd0ac-107">[InkEdit](inkedit-control-reference.md)控制項的主要目的是要收集筆跡、加以辨識，並以文字形式顯示。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="dd0ac-108">此外，它支援將筆墨顯示為具有文字格式設定功能的内嵌物件，例如粗體和底線。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="dd0ac-109">手勢和修正</span><span class="sxs-lookup"><span data-stu-id="dd0ac-109">Gestures and Correction</span></span>

<span data-ttu-id="dd0ac-110">[InkEdit](inkedit-control-reference.md) 支援下列手勢。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="dd0ac-111">手勢</span><span class="sxs-lookup"><span data-stu-id="dd0ac-111">Gesture</span></span>                                                                    | <span data-ttu-id="dd0ac-112">手勢名稱</span><span class="sxs-lookup"><span data-stu-id="dd0ac-112">Gesture Name</span></span>              | <span data-ttu-id="dd0ac-113">動作</span><span class="sxs-lookup"><span data-stu-id="dd0ac-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![向左手勢](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="dd0ac-115">向左</span><span class="sxs-lookup"><span data-stu-id="dd0ac-115">Down-left</span></span><br/>      | <span data-ttu-id="dd0ac-116">Enter</span><span class="sxs-lookup"><span data-stu-id="dd0ac-116">Enter</span></span><br/>     |
| ![向左移長的手勢](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="dd0ac-118">向左至左-long</span><span class="sxs-lookup"><span data-stu-id="dd0ac-118">Down-left-long</span></span><br/> | <span data-ttu-id="dd0ac-119">Enter</span><span class="sxs-lookup"><span data-stu-id="dd0ac-119">Enter</span></span><br/>     |
| ![右上手勢](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="dd0ac-121">右上方</span><span class="sxs-lookup"><span data-stu-id="dd0ac-121">Up-right</span></span><br/>       | <span data-ttu-id="dd0ac-122">索引標籤</span><span class="sxs-lookup"><span data-stu-id="dd0ac-122">Tab</span></span><br/>       |
| ![最右側的手勢。](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="dd0ac-124">右上-long</span><span class="sxs-lookup"><span data-stu-id="dd0ac-124">Up-right-long</span></span><br/>  | <span data-ttu-id="dd0ac-125">索引標籤</span><span class="sxs-lookup"><span data-stu-id="dd0ac-125">Tab</span></span><br/>       |
| ![右手勢](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="dd0ac-127">Right</span><span class="sxs-lookup"><span data-stu-id="dd0ac-127">Right</span></span><br/>          | <span data-ttu-id="dd0ac-128">Space</span><span class="sxs-lookup"><span data-stu-id="dd0ac-128">Space</span></span><br/>     |
| ![左方手勢](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="dd0ac-130">Left</span><span class="sxs-lookup"><span data-stu-id="dd0ac-130">Left</span></span><br/>           | <span data-ttu-id="dd0ac-131">退格鍵</span><span class="sxs-lookup"><span data-stu-id="dd0ac-131">Backspace</span></span><br/> |



 

<span data-ttu-id="dd0ac-132">您可以處理的手勢事件包含手勢、筆劃和游標資訊，您可以用來傳送文字以 [InkEdit](inkedit-control-reference.md) 或將資料放在剪貼簿上。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="dd0ac-133">[InkEdit](inkedit-control-reference.md) 也提供更正使用者介面，可讓使用者從替代項中進行流覽和選取、使用螢幕小鍵盤，以及字元/字母/封鎖辨識器。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="dd0ac-134">其他詳細資料</span><span class="sxs-lookup"><span data-stu-id="dd0ac-134">Other Details</span></span>

<span data-ttu-id="dd0ac-135">[InkEdit](inkedit-control-reference.md) 的設計可在單一行的表單案例中，以及多行文字輸入和編輯的情況下運作。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="dd0ac-136">InkEdit 的主要用途是從使用者以手寫形式取得文字輸入。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="dd0ac-137">根據預設，會辨識筆跡輸入，並在其位置插入文字。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="dd0ac-138">InkEdit 的預設使用者介面類別似于 [**RichTextBox**](/previous-versions/windows/) 控制項，但使用者正在配置筆墨時除外。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="dd0ac-139">您可以顯示原始筆跡而非文字;不過，筆墨會調整為 InkEdit 控制項目前的輸入字型大小，並以內嵌方式顯示在其他文字中。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="dd0ac-140">基於安全性考慮，您必須使用標準程式來開啟或關閉檔案、串流輸入/輸出，以及設定 [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) 或 [**文本**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) 屬性。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="dd0ac-141">[InkEdit](inkedit-control-reference.md)控制項預設會設定為將筆墨辨識為文字。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="dd0ac-142">若要讓使用者將筆墨新增為筆墨，請將 [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) 屬性設定為 **InsertAsInk**。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="dd0ac-143">如需 [InkEdit](inkedit-control-reference.md) 控制項的詳細參考資訊，請參閱 InkEdit。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="dd0ac-144">如果您使用 Win32 [InkEdit](inkedit-control-reference.md) 控制項，並將它放在群組方塊內，請確定方塊具有透明樣式;否則，InkEdit 就無法收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="dd0ac-145">若要確保筆墨正確顯示，請在收到 [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1)或 [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1)事件時呼叫 [InkEdit](inkedit-control-reference.md) [**控制項重新**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh)整理方法。</span><span class="sxs-lookup"><span data-stu-id="dd0ac-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="dd0ac-146">下列各節詳細說明 [InkEdit](inkedit-control-reference.md) 控制項的使用：</span><span class="sxs-lookup"><span data-stu-id="dd0ac-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="dd0ac-147">具現化 InkEdit</span><span class="sxs-lookup"><span data-stu-id="dd0ac-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="dd0ac-148">單字與字元識別的比較</span><span class="sxs-lookup"><span data-stu-id="dd0ac-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="dd0ac-149">將筆墨顯示為筆墨</span><span class="sxs-lookup"><span data-stu-id="dd0ac-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="dd0ac-150">在舊版 Windows 上使用 InkEdit</span><span class="sxs-lookup"><span data-stu-id="dd0ac-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="dd0ac-151">使用應用程式字典搭配 InkEdit</span><span class="sxs-lookup"><span data-stu-id="dd0ac-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

