---
title: 像素格式
description: 像素格式
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- Windows 上的 OpenGL，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968063"
---
# <a name="pixel-formats"></a><span data-ttu-id="ff408-104">像素格式</span><span class="sxs-lookup"><span data-stu-id="ff408-104">Pixel Formats</span></span>

<span data-ttu-id="ff408-105">*像素格式* 會指定 OpenGL 繪圖介面的數個屬性。</span><span class="sxs-lookup"><span data-stu-id="ff408-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="ff408-106">像素格式所指定的部分屬性如下：</span><span class="sxs-lookup"><span data-stu-id="ff408-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="ff408-107">圖元緩衝區為單一或雙重緩衝。</span><span class="sxs-lookup"><span data-stu-id="ff408-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="ff408-108">圖元資料是否在 RGBA 或色彩索引表單中。</span><span class="sxs-lookup"><span data-stu-id="ff408-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="ff408-109">用來儲存色彩資料的位數目。</span><span class="sxs-lookup"><span data-stu-id="ff408-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="ff408-110">用於深度 (Z 軸) 緩衝區的位數。</span><span class="sxs-lookup"><span data-stu-id="ff408-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="ff408-111">用於樣板緩衝區的位數目。</span><span class="sxs-lookup"><span data-stu-id="ff408-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="ff408-112">重迭和基礎平面的數目。</span><span class="sxs-lookup"><span data-stu-id="ff408-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="ff408-113">各種可見度遮罩。</span><span class="sxs-lookup"><span data-stu-id="ff408-113">Various visibility masks.</span></span>

<span data-ttu-id="ff408-114">Microsoft 的適用于 Windows 的 OpenGL 執行會使用 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構來傳達像素格式資料。</span><span class="sxs-lookup"><span data-stu-id="ff408-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="ff408-115">結構的成員會指定先前的屬性和其他數個屬性。</span><span class="sxs-lookup"><span data-stu-id="ff408-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="ff408-116">給定的裝置內容可以支援數個像素格式。</span><span class="sxs-lookup"><span data-stu-id="ff408-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="ff408-117">Windows 會以連續的單一索引值（ (1、2、3、4等等）來識別裝置內容所支援的像素格式，) 。</span><span class="sxs-lookup"><span data-stu-id="ff408-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="ff408-118">裝置內容只能有一個目前的像素格式，可從它所支援的像素格式集合中選擇。</span><span class="sxs-lookup"><span data-stu-id="ff408-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="ff408-119">在 Windows 中，每個視窗都有它自己目前的像素格式。</span><span class="sxs-lookup"><span data-stu-id="ff408-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="ff408-120">例如，這表示應用程式可以同時顯示 RGBA 和色彩索引 OpenGL 視窗，或單一和雙重緩衝的 OpenGL 視窗。</span><span class="sxs-lookup"><span data-stu-id="ff408-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="ff408-121">這個每個視窗的像素格式功能僅限於 OpenGL 視窗。</span><span class="sxs-lookup"><span data-stu-id="ff408-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="ff408-122">通常，您會取得裝置內容、設定裝置內容的像素格式，然後建立適用于該裝置的 OpenGL 轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="ff408-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="ff408-123">您可以在建立轉譯內容之前設定像素格式，因為轉譯內容會繼承裝置內容的像素格式。</span><span class="sxs-lookup"><span data-stu-id="ff408-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ff408-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff408-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff408-125">像素格式函數</span><span class="sxs-lookup"><span data-stu-id="ff408-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




