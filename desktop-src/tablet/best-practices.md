---
description: 使用 [畫筆輸入面板] 物件時的最佳作法總覽。
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: " (Tablet PC) 的最佳作法"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195324"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="fa20e-103"> (Tablet PC) 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="fa20e-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="fa20e-104">使用 [**PenInputPanel**](peninputpanel-class.md) 物件時，請記住一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="fa20e-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="fa20e-105">偏好 InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="fa20e-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="fa20e-106">停用 InkEdit 控制項的筆墨模式</span><span class="sxs-lookup"><span data-stu-id="fa20e-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="fa20e-107">使用無視窗控制項</span><span class="sxs-lookup"><span data-stu-id="fa20e-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="fa20e-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa20e-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="fa20e-109">偏好 InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="fa20e-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="fa20e-110">[InkEdit](inkedit-control-reference.md) 是要附加 [**PenInputPanel**](peninputpanel-class.md) 物件的慣用控制項。</span><span class="sxs-lookup"><span data-stu-id="fa20e-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="fa20e-111">InkEdit 控制項提供 [文字服務架構 (TSF) ](text-services-framework.md)的支援。</span><span class="sxs-lookup"><span data-stu-id="fa20e-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="fa20e-112">停用 InkEdit 控制項的筆墨模式</span><span class="sxs-lookup"><span data-stu-id="fa20e-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="fa20e-113">附加至 [InkEdit](inkedit-control-reference.md) 控制項時，請將 InkEdit 控制項的 [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) 屬性設定為 [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) 值。</span><span class="sxs-lookup"><span data-stu-id="fa20e-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="fa20e-114">如果 [ **InkMode** ] 屬性未設定為 [ **InkMode** ] 值，則 InkEdit 控制項會將第一點點轉譯為筆劃、將其傳遞至辨識器，然後將文字插入 InkEdit 控制項中。</span><span class="sxs-lookup"><span data-stu-id="fa20e-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="fa20e-115">因為您已經附加 [**PenInputPanel**](peninputpanel-class.md) 物件來接受筆跡輸入，所以不需要也為筆墨輸入啟用 InkEdit 控制項。</span><span class="sxs-lookup"><span data-stu-id="fa20e-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="fa20e-116">使用無視窗控制項</span><span class="sxs-lookup"><span data-stu-id="fa20e-116">Using Windowless Controls</span></span>

<span data-ttu-id="fa20e-117">將 [**PenInputPanel**](peninputpanel-class.md) 物件附加至包含多個無視窗控制項的父視窗時， **PenInputPanel** 物件不知道如何在將焦點移到無視窗的子系時追蹤插入號。</span><span class="sxs-lookup"><span data-stu-id="fa20e-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="fa20e-118">當輸入暫止時，當焦點從一個無視窗控制項移至另一個控制項時，手寫輸入可以傳送至錯誤的子系。</span><span class="sxs-lookup"><span data-stu-id="fa20e-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="fa20e-119">若要在無視窗環境中使用 [**PenInputPanel**](peninputpanel-class.md) 物件，您可以使用下列技術：</span><span class="sxs-lookup"><span data-stu-id="fa20e-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="fa20e-120">將 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) 控制項具現化，並將它放在無視窗控制項上。</span><span class="sxs-lookup"><span data-stu-id="fa20e-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="fa20e-121">將 [**PenInputPanel**](peninputpanel-class.md) 物件附加至新的文字方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="fa20e-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="fa20e-122">讓文字方塊控制項收集 [**PenInputPanel**](peninputpanel-class.md) 物件中的已辨識文字。</span><span class="sxs-lookup"><span data-stu-id="fa20e-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="fa20e-123">當焦點變更離開文字方塊控制項時，呼叫 [**PenInputPanel**](peninputpanel-class.md)物件的 [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput)方法。</span><span class="sxs-lookup"><span data-stu-id="fa20e-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="fa20e-124">將已辨識的文字從文字方塊控制項複製到無視窗子系。</span><span class="sxs-lookup"><span data-stu-id="fa20e-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="fa20e-125">將 [**PenInputPanel**](peninputpanel-class.md) 物件的 [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (僅限 managed 程式碼) 屬性或 [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) 屬性設定為 null，以卸離該物件。</span><span class="sxs-lookup"><span data-stu-id="fa20e-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="fa20e-126">終結文字方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="fa20e-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa20e-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa20e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa20e-128">**PenInputPanel 類別**</span><span class="sxs-lookup"><span data-stu-id="fa20e-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="fa20e-129">[PenInputPanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="fa20e-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="fa20e-130">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="fa20e-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
