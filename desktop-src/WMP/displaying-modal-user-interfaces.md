---
title: 顯示模式使用者介面
description: 顯示模式使用者介面
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player 外掛程式，顯示對話方塊和訊息方塊
- 外掛程式，顯示對話方塊和訊息方塊
- 使用者介面外掛程式，顯示對話方塊和訊息方塊
- UI 外掛程式，顯示對話方塊和訊息方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675884"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="ac170-107">顯示模式使用者介面</span><span class="sxs-lookup"><span data-stu-id="ac170-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="ac170-108">UI 外掛程式不應顯示模式對話方塊或訊息方塊，以回應來自 Windows Media Player 的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="ac170-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="ac170-109">例如，請勿從 **IWMPPluginUI：： Create** 的執行顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="ac170-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="ac170-110">如果您必須從播放程式所呼叫的 UI 外掛程式方法執行中顯示對話方塊或訊息方塊，則必須遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="ac170-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="ac170-111">使用 **RegisterWindowMessage** 註冊新的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="ac170-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="ac170-112">使用 **PostMessage** 將您註冊的視窗訊息傳送至 UI 外掛程式視窗。</span><span class="sxs-lookup"><span data-stu-id="ac170-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="ac170-113">從訊息處理常式顯示新視窗訊息的對話方塊或訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="ac170-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac170-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac170-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac170-115">**UI 外掛程式總覽**</span><span class="sxs-lookup"><span data-stu-id="ac170-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




