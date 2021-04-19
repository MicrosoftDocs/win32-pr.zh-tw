---
description: Uniscribe 會將 Unicode (cmap 儲存) 對應、圖像寬度和 OpenType 腳本成形資料表。
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: '快取 (國際化) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992206"
---
# <a name="caching-internationalization"></a><span data-ttu-id="bc2e7-103">快取 (國際化) </span><span class="sxs-lookup"><span data-stu-id="bc2e7-103">Caching (Internationalization)</span></span>

<span data-ttu-id="bc2e7-104">Uniscribe 會將 Unicode (cmap 儲存) 對應、圖像寬度和 OpenType 腳本成形資料表。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-104">Uniscribe saves Unicode-to-glyph (cmap) mappings, glyph widths, and OpenType script shaping tables.</span></span> <span data-ttu-id="bc2e7-105">特定大小之特定字型的資料表控制碼稱為「腳本快取」。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-105">A handle to the tables for a particular font of a particular size is called a "script cache".</span></span> <span data-ttu-id="bc2e7-106">許多 Uniscribe 函式會呼叫裝置內容控制碼參數和腳本快取結構 [**\_**](script-cache.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-106">Many Uniscribe functions call for both a device context handle parameter and a pointer to a [**SCRIPT\_CACHE**](script-cache.md) structure.</span></span> <span data-ttu-id="bc2e7-107">這些函式會先查看腳本快取的資訊，只有在需要的資料表尚未快取時，才會使用裝置內容。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-107">These functions look first for information through the script cache, using the device context only when required tables are not already cached.</span></span> <span data-ttu-id="bc2e7-108">呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)、 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)或 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) 函式時，應用程式必須將指標傳遞至腳本快 **取 \_** 結構。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-108">When calling the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), or [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) function, the application must pass a pointer to a **SCRIPT\_CACHE** structure.</span></span> <span data-ttu-id="bc2e7-109">當應用程式第一次將它傳遞給 Uniscribe 函式之前，應該將控制碼初始化為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-109">The handle should be initialized to **NULL** before the first time the application passes it to a Uniscribe function.</span></span> <span data-ttu-id="bc2e7-110">應用程式絕對不應針對不同的字型或不同的大小傳遞相同的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-110">The application should never pass the same handle for different fonts or different sizes.</span></span>

<span data-ttu-id="bc2e7-111">應用程式可以在任何時間釋放腳本快取。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-111">An application can free a script cache at any time.</span></span> <span data-ttu-id="bc2e7-112">Uniscribe 會維護其字型和整形程式快取中的參考計數，只有在所有字型的大小都釋出時，才會釋出字型資料，而且只有當支援程式的所有字型都釋出時，才會釋出資料。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-112">Uniscribe maintains reference counts in its font and shaper caches, frees font data only when all sizes of the font are freed, and frees shaper data only when all fonts that the shaper supports are freed.</span></span> <span data-ttu-id="bc2e7-113">當應用程式使用樣式完成時，應該呼叫 [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) 函式來釋放樣式的腳本快取。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-113">When the application is done with a style, it should call the [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) function to free the script cache for the style.</span></span>

<span data-ttu-id="bc2e7-114">針對 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 和 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)，應用程式有效地傳遞 null 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-114">For [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) and [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), it is valid for the application to pass a null device context.</span></span> <span data-ttu-id="bc2e7-115">最常呼叫會成功，因為已快取所需的資料表。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-115">Most often the call will succeed, as required tables are already cached.</span></span> <span data-ttu-id="bc2e7-116">如果成形或位置需要存取裝置內容， **ScriptShape** 或 **ScriptPlace** 會立即傳回電子 \_ 暫止錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-116">If the shaping or placement requires access to a device context, **ScriptShape** or **ScriptPlace** returns immediately with the E\_PENDING error code.</span></span> <span data-ttu-id="bc2e7-117">然後，應用程式必須選取裝置內容中的字型。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-117">Then the application must select the font in the device context.</span></span> <span data-ttu-id="bc2e7-118">在大部分的應用程式中，這可避免重複使用 [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject)的呼叫來準備裝置內容控制碼，以協助效能。</span><span class="sxs-lookup"><span data-stu-id="bc2e7-118">For most applications, this helps performance by avoiding repeated preparation of a device context handle with calls to [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc2e7-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc2e7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc2e7-120">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="bc2e7-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
