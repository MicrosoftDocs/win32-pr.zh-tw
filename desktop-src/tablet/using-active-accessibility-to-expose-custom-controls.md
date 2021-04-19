---
description: 使用主動式存取範圍來公開 Tablet PC 自訂控制項的描述。
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: 使用 Active Accessibility 來公開自訂控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972401"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="6c7b7-103">使用 Active Accessibility 來公開自訂控制項</span><span class="sxs-lookup"><span data-stu-id="6c7b7-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="6c7b7-104">您可以使用 Microsoft Active Accessibility 作為讓自訂控制項與協助工具輔助相容的有效方式。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="6c7b7-105">Active Accessibility 需要應用程式：</span><span class="sxs-lookup"><span data-stu-id="6c7b7-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="6c7b7-106">建立元件物件模型 (COM) 物件，這些物件代表個別的自訂控制項或正確支援 **IAccessible** 介面的控制項群組。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="6c7b7-107"> (當 Active Accessibility 用戶端要求物件時，可能會視需要建立物件。 ) </span><span class="sxs-lookup"><span data-stu-id="6c7b7-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="6c7b7-108">當控制項建立或損毀、獲得或失去焦點，或變更狀態時，呼叫 [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) 。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="6c7b7-109">\_用來查詢物件或物件的屬性時，處理 WM GETOBJECT 訊息。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="6c7b7-110">基於本文的目的，也需要公開一個包含其他自訂物件的視窗來 Active Accessibility，讓用戶端可以探索並流覽至子物件。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="6c7b7-111">如需如何使自訂控制項與協助工具協助工具相容的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="6c7b7-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
