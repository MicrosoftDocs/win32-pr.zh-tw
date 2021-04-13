---
title: 使用裝置內容
description: 使用裝置內容
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- 視覺效果，裝置內容
- 自訂視覺效果，裝置內容
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函式，裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301147"
---
# <a name="using-device-contexts"></a><span data-ttu-id="aa385-108">使用裝置內容</span><span class="sxs-lookup"><span data-stu-id="aa385-108">Using Device Contexts</span></span>

<span data-ttu-id="aa385-109">裝置內容是裝置內容的標準控點。</span><span class="sxs-lookup"><span data-stu-id="aa385-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="aa385-110">許多繪圖功能都需要此功能，讓 Microsoft Windows 知道要在哪一個視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="aa385-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="aa385-111">例如，若要繪製矩形，您必須指定裝置內容。</span><span class="sxs-lookup"><span data-stu-id="aa385-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="aa385-112">裝置內容是由 Windows Media Player 透過 **Render** 函式指定。</span><span class="sxs-lookup"><span data-stu-id="aa385-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="aa385-113">如果您的外掛程式使用視窗轉譯，您將需要使用該視窗的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="aa385-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="aa385-114">針對需要裝置內容的任何繪圖工具，請使用此裝置內容。</span><span class="sxs-lookup"><span data-stu-id="aa385-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa385-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa385-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa385-116">**執行轉譯**</span><span class="sxs-lookup"><span data-stu-id="aa385-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




