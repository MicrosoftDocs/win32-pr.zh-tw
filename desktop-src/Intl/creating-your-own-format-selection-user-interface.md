---
description: 國際文字顯示
ms.assetid: e6cc5169-1a6e-40f8-b616-e76ec919195c
title: 國際文字顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8ba7eb6f1a043bb642945e178f3545bcd51738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027361"
---
# <a name="international-text-display"></a><span data-ttu-id="79a9b-103">國際文字顯示</span><span class="sxs-lookup"><span data-stu-id="79a9b-103">International Text Display</span></span>

<span data-ttu-id="79a9b-104">有四個可能的選項可用來顯示國際文字，而這也需要複雜字集的輸出：</span><span class="sxs-lookup"><span data-stu-id="79a9b-104">There are four possible options for displaying international text, which also entails the output of complex scripts:</span></span>

-   <span data-ttu-id="79a9b-105">呼叫 Windows 文字 Api</span><span class="sxs-lookup"><span data-stu-id="79a9b-105">Calling Windows text APIs</span></span>
-   <span data-ttu-id="79a9b-106">具現化 Windows 標準編輯控制項</span><span class="sxs-lookup"><span data-stu-id="79a9b-106">Instantiating Windows standard edit controls</span></span>
-   <span data-ttu-id="79a9b-107">具現化 rich edit 控制項</span><span class="sxs-lookup"><span data-stu-id="79a9b-107">Instantiating rich edit controls</span></span>
-   <span data-ttu-id="79a9b-108">呼叫 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="79a9b-108">Calling Uniscribe</span></span>

<span data-ttu-id="79a9b-109">如需這些選項的說明和優點，請參閱 [顯示文字的選項](https://msdn.microsoft.com/globalization/mt662335) 。</span><span class="sxs-lookup"><span data-stu-id="79a9b-109">Please see [Options for Displaying Text](https://msdn.microsoft.com/globalization/mt662335) for the explanation and advantages of each of these options.</span></span> <span data-ttu-id="79a9b-110">然後，您可以根據應用程式的複雜度和其設計功能，決定哪一個是您應用程式的最佳選項。</span><span class="sxs-lookup"><span data-stu-id="79a9b-110">It is then up to you to decide which is the best option for your application, based on the application's complexity and its design features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79a9b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="79a9b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79a9b-112">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="79a9b-112">**TextOut**</span></span>](/windows/win32/api/wingdi/nf-wingdi-textouta)
</dt> <dt>

[<span data-ttu-id="79a9b-113">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="79a9b-113">**ExtTextOut**</span></span>](/windows/win32/api/wingdi/nf-wingdi-exttextouta)
</dt> <dt>

[<span data-ttu-id="79a9b-114">**TabbedTextOut**</span><span class="sxs-lookup"><span data-stu-id="79a9b-114">**TabbedTextOut**</span></span>](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)
</dt> <dt>

[<span data-ttu-id="79a9b-115">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="79a9b-115">**DrawText**</span></span>](/windows/win32/api/winuser/nf-winuser-drawtext)
</dt> <dt>

[<span data-ttu-id="79a9b-116">**GetTabbedTextExtent**</span><span class="sxs-lookup"><span data-stu-id="79a9b-116">**GetTabbedTextExtent**</span></span>](/windows/win32/api/winuser/nf-winuser-gettabbedtextextenta)
</dt> <dt>

[<span data-ttu-id="79a9b-117">**GetTextExtentPoint32**</span><span class="sxs-lookup"><span data-stu-id="79a9b-117">**GetTextExtentPoint32**</span></span>](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)
</dt> <dt>

[<span data-ttu-id="79a9b-118">**GetTextExtentExPoint**</span><span class="sxs-lookup"><span data-stu-id="79a9b-118">**GetTextExtentExPoint**</span></span>](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)
</dt> <dt>

[<span data-ttu-id="79a9b-119">**編輯控制項**</span><span class="sxs-lookup"><span data-stu-id="79a9b-119">**Edit control**</span></span>](../msi/edit-control.md)
</dt> <dt>

[<span data-ttu-id="79a9b-120">Rich Edit</span><span class="sxs-lookup"><span data-stu-id="79a9b-120">Rich Edit</span></span>](../controls/about-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="79a9b-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="79a9b-121">Uniscribe</span></span>](uniscribe.md)
</dt> </dl>

 

 
