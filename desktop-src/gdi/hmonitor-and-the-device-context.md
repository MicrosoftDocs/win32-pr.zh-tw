---
description: 每個實體顯示器都會以 HMONITOR 類型的監視器控制碼表示。
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR 和裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991214"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="0aa92-103">HMONITOR 和裝置內容</span><span class="sxs-lookup"><span data-stu-id="0aa92-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="0aa92-104">每個實體顯示器都會以 **HMONITOR** 類型的監視器控制碼表示。</span><span class="sxs-lookup"><span data-stu-id="0aa92-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="0aa92-105">有效的 **HMONITOR** 保證為非 Null。</span><span class="sxs-lookup"><span data-stu-id="0aa92-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="0aa92-106">實體顯示器具有相同的 **HMONITOR** ，只要它是桌面的一部分。</span><span class="sxs-lookup"><span data-stu-id="0aa92-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="0aa92-107">傳送 **WM \_ DISPLAYCHANGE** 訊息時，可能會從桌面上移除任何監視器，因此其 **HMONITOR** 會變成無效或其設定已變更。</span><span class="sxs-lookup"><span data-stu-id="0aa92-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="0aa92-108">因此，應用程式應該在傳送此訊息時，檢查所有 **HMONITORS** 是否有效。</span><span class="sxs-lookup"><span data-stu-id="0aa92-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="0aa92-109">任何會傳回顯示裝置內容 (DC) 的函式通常會傳回主要監視的 DC。</span><span class="sxs-lookup"><span data-stu-id="0aa92-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="0aa92-110">若要取得其他監視器的 DC，請使用 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) 函數。</span><span class="sxs-lookup"><span data-stu-id="0aa92-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="0aa92-111">或者，您可以使用 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) 函式中的裝置名稱，建立具有 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)的 DC。</span><span class="sxs-lookup"><span data-stu-id="0aa92-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="0aa92-112">但是，如果函式（例如 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)）取得跨越多個顯示之視窗的 dc，則 dc 也會橫跨這兩個顯示。</span><span class="sxs-lookup"><span data-stu-id="0aa92-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



