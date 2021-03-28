---
description: Windows GDI + 是以類別為基礎的 API，適用于 C/c + + 程式設計人員。
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112952"
---
# <a name="gdi"></a><span data-ttu-id="7475f-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="7475f-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="7475f-104">目的</span><span class="sxs-lookup"><span data-stu-id="7475f-104">Purpose</span></span>

<span data-ttu-id="7475f-105">Windows GDI + 是以類別為基礎的 API，適用于 C/c + + 程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="7475f-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="7475f-106">它可讓應用程式在影片顯示器和印表機上使用圖形和格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="7475f-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="7475f-107">以 Microsoft Win32 API 為基礎的應用程式不會直接存取圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="7475f-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="7475f-108">相反地，GDI+ 會代表應用程式與裝置驅動程式進行互動。</span><span class="sxs-lookup"><span data-stu-id="7475f-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="7475f-109">Microsoft Win64 也支援 GDI+。</span><span class="sxs-lookup"><span data-stu-id="7475f-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7475f-110">適用時</span><span class="sxs-lookup"><span data-stu-id="7475f-110">Where applicable</span></span>

<span data-ttu-id="7475f-111">在 Windows 服務中不支援使用 GDI + 函式和類別。</span><span class="sxs-lookup"><span data-stu-id="7475f-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="7475f-112">嘗試從 Windows 服務使用這些函式和類別可能會產生未預期的問題，例如服務效能降低、執行時間例外狀況或錯誤。</span><span class="sxs-lookup"><span data-stu-id="7475f-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="7475f-113">當您使用 GDI + API 時，您絕不能讓應用程式從不受信任的來源下載任意字型。</span><span class="sxs-lookup"><span data-stu-id="7475f-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="7475f-114">作業系統需要較高的許可權，以確保所有已安裝的字型都受到信任。</span><span class="sxs-lookup"><span data-stu-id="7475f-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7475f-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="7475f-115">Developer audience</span></span>

<span data-ttu-id="7475f-116">GDI + c + + 類別型介面是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="7475f-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="7475f-117">需要熟悉 Windows 圖形使用者介面和訊息驅動架構。</span><span class="sxs-lookup"><span data-stu-id="7475f-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7475f-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="7475f-118">Run-time requirements</span></span>

<span data-ttu-id="7475f-119">GDI + 可以在所有 Windows 應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="7475f-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="7475f-120">GDI + 是在 Windows XP 和 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="7475f-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7475f-121">如需有關使用特定類別或方法的作業系統需要哪些作業系統的詳細資訊，請參閱類別或方法檔集的詳細資訊一節。</span><span class="sxs-lookup"><span data-stu-id="7475f-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7475f-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="7475f-122">In this section</span></span>

| <span data-ttu-id="7475f-123">主題</span><span class="sxs-lookup"><span data-stu-id="7475f-123">Topic</span></span>                                                    | <span data-ttu-id="7475f-124">描述</span><span class="sxs-lookup"><span data-stu-id="7475f-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="7475f-125">概觀</span><span class="sxs-lookup"><span data-stu-id="7475f-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="7475f-126">關於 GDI + 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="7475f-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="7475f-127">使用</span><span class="sxs-lookup"><span data-stu-id="7475f-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="7475f-128">使用 GDI + 的工作和範例。</span><span class="sxs-lookup"><span data-stu-id="7475f-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="7475f-129">參考</span><span class="sxs-lookup"><span data-stu-id="7475f-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="7475f-130">GDI + c + + 類別型 API 的檔。</span><span class="sxs-lookup"><span data-stu-id="7475f-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="7475f-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7475f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7475f-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="7475f-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="7475f-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7475f-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7475f-134">Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="7475f-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="7475f-135">Opengl</span><span class="sxs-lookup"><span data-stu-id="7475f-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="7475f-136">Windows 多媒體</span><span class="sxs-lookup"><span data-stu-id="7475f-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
