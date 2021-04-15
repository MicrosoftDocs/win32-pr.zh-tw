---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463116"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="bedb2-103">IAgentEx::ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="bedb2-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="bedb2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bedb2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="bedb2-105">顯示 [預設字元屬性] 視窗。</span><span class="sxs-lookup"><span data-stu-id="bedb2-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="bedb2-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="bedb2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bedb2-107"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="bedb2-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="bedb2-108">視窗的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="bedb2-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="bedb2-109"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="bedb2-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="bedb2-110">視窗的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="bedb2-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="bedb2-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span><span class="sxs-lookup"><span data-stu-id="bedb2-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="bedb2-112">預設位置旗標。</span><span class="sxs-lookup"><span data-stu-id="bedb2-112">Default position flag.</span></span> <span data-ttu-id="bedb2-113">如果此參數為 **True**，Microsoft Agent 會在其顯示的最後一個位置顯示預設字元的屬性工作表視窗。</span><span class="sxs-lookup"><span data-stu-id="bedb2-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="bedb2-114">針對 Windows 2000，您可能需要呼叫新的 [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API，以確保此視窗成為前景視窗。</span><span class="sxs-lookup"><span data-stu-id="bedb2-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="bedb2-115">如需有關在 Windows 2000 下設定前景視窗的詳細資訊，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="bedb2-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bedb2-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bedb2-116">See Also</span></span>

[<span data-ttu-id="bedb2-117">**IAgentNotifySinkEx：:D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="bedb2-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 