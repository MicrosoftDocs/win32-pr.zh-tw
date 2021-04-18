---
description: 狀態、撰寫和候選視窗會形成 IME 的使用者介面。
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: 狀態、撰寫和候選視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b800def67299a464fd232a08a2bbff0a2a60a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195287"
---
# <a name="status-composition-and-candidates-windows"></a><span data-ttu-id="606b8-103">狀態、撰寫和候選視窗</span><span class="sxs-lookup"><span data-stu-id="606b8-103">Status, Composition, and Candidates Windows</span></span>

<span data-ttu-id="606b8-104">狀態、撰寫和候選視窗會形成 IME 的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="606b8-104">The status, composition, and candidates windows form the user interface for the IME.</span></span> <span data-ttu-id="606b8-105">狀態視窗指出 IME 已開啟，並提供使用者設定轉換模式的方法。</span><span class="sxs-lookup"><span data-stu-id="606b8-105">The status window indicates that the IME is open and provides the user with the means to set the conversion modes.</span></span> <span data-ttu-id="606b8-106">當使用者輸入文字時會出現組合視窗，而且根據轉換模式，會將文字顯示為輸入或顯示轉換的文字。</span><span class="sxs-lookup"><span data-stu-id="606b8-106">The composition window appears when the user enters text and, depending on the conversion mode, either displays the text as entered or displays converted text.</span></span> <span data-ttu-id="606b8-107">候選視窗會與撰寫視窗一起出現。</span><span class="sxs-lookup"><span data-stu-id="606b8-107">The candidates window appears in conjunction with the composition window.</span></span> <span data-ttu-id="606b8-108">它包含在組合視窗中選取的字元) 的「候選」 (替代字元」清單。</span><span class="sxs-lookup"><span data-stu-id="606b8-108">It contains a list of "candidates" (alternative characters) for the selected character or characters in the composition window.</span></span> <span data-ttu-id="606b8-109">使用者可以在候選清單中移動，然後選取所需的字元，再回到撰寫視窗。</span><span class="sxs-lookup"><span data-stu-id="606b8-109">The user can scroll through the candidates list and select the desired characters, then return to the composition window.</span></span> <span data-ttu-id="606b8-110">使用者可以用這種方式撰寫所要的文字，直到組合字元串完成並關閉視窗為止。</span><span class="sxs-lookup"><span data-stu-id="606b8-110">The user can compose the desired text in this way until the composition string is finalized and the window is closed.</span></span>

<span data-ttu-id="606b8-111">IME 會以 [**WM \_ ime \_ 字元**](wm-ime-char.md) 或 [**wm \_ ime \_ 組合**](wm-ime-composition.md)/GCS 結果訊息的形式，將組成的字元傳送至 IME 感知的應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="606b8-111">The IME sends the composed characters to the IME-aware application in the form of [**WM\_IME\_CHAR**](wm-ime-char.md) or [**WM\_IME\_COMPOSITION**](wm-ime-composition.md)/GCS\_RESULT messages.</span></span> <span data-ttu-id="606b8-112">如果應用程式不會處理這些訊息， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將它們轉譯成一或多個 [**WM \_ 字元**](../inputdev/wm-char.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="606b8-112">If the application does not process these messages, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function translates them into one or more [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span>

<span data-ttu-id="606b8-113">根據預設，作業系統會自動建立並管理文字輸入需求的狀態、撰寫和候選視窗。</span><span class="sxs-lookup"><span data-stu-id="606b8-113">By default, the operating system automatically creates and manages status, composition, and candidates windows for text input requirements.</span></span> <span data-ttu-id="606b8-114">對於許多應用程式而言，此預設處理已足夠。</span><span class="sxs-lookup"><span data-stu-id="606b8-114">For many applications, this default processing is sufficient.</span></span> <span data-ttu-id="606b8-115">這些應用程式完全依賴于作業系統進行 IME 支援，而且稱為「IME 感知」，因為它們不知道作業系統執行以管理 IME 視窗的許多工。</span><span class="sxs-lookup"><span data-stu-id="606b8-115">These applications rely entirely on the operating system for IME support and are said to be "IME-unaware" because they are unaware of the many tasks the operating system carries out to manage the IME windows.</span></span>

<span data-ttu-id="606b8-116">另一方面，IME 感知的應用程式會參與建立和管理 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="606b8-116">An IME-aware application, on the other hand, participates in the creation and management of IME windows.</span></span> <span data-ttu-id="606b8-117">這類應用程式會藉由將訊息傳送至這些視窗，以及攔截和處理來自 windows 的訊息，來控制預設視窗的操作、位置和外觀。</span><span class="sxs-lookup"><span data-stu-id="606b8-117">Such applications control the operation, position, and appearance of the default windows by sending messages to these windows and by intercepting and processing messages from the windows.</span></span> <span data-ttu-id="606b8-118">在某些情況下，應用程式會建立自己的 IME 視窗，並為其自訂狀態、撰寫和候選視窗提供完整的處理。</span><span class="sxs-lookup"><span data-stu-id="606b8-118">In some cases, applications create their own IME windows and provide complete processing for their custom status, composition, and candidates windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="606b8-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="606b8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="606b8-120">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="606b8-120">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
