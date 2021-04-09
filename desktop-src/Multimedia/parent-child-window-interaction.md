---
title: Parent-Child 視窗互動
description: Parent-Child 視窗互動
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681998"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="e9f5f-103">Parent-Child 視窗互動</span><span class="sxs-lookup"><span data-stu-id="e9f5f-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="e9f5f-104">某些系統層級的訊息，例如 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)，只會傳送到最上層和重迭的視窗。</span><span class="sxs-lookup"><span data-stu-id="e9f5f-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="e9f5f-105">如果捕捉視窗是子視窗，其父系必須轉送這些訊息。</span><span class="sxs-lookup"><span data-stu-id="e9f5f-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="e9f5f-106">同樣地，如果父視窗變更大小，可能需要將通知訊息傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="e9f5f-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="e9f5f-107">相反地，如果已捕捉的影片的維度變更，則 [捕獲] 視窗可能需要將通知訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="e9f5f-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="e9f5f-108">管理這項工作最簡單的方式，就是一律讓 [捕捉視窗] 維度等於已捕捉的影片資料流程大小，並在這些維度變更時通知父代。</span><span class="sxs-lookup"><span data-stu-id="e9f5f-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9f5f-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9f5f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9f5f-110">捕獲 Windows</span><span class="sxs-lookup"><span data-stu-id="e9f5f-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 