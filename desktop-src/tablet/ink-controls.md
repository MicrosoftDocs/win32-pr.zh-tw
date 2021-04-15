---
description: Tablet PC 的筆墨控制項總覽。
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: 筆墨控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511305"
---
# <a name="ink-controls"></a><span data-ttu-id="4aa1d-103">筆墨控制項</span><span class="sxs-lookup"><span data-stu-id="4aa1d-103">Ink Controls</span></span>

<span data-ttu-id="4aa1d-104">Tablet PC 平臺提供兩種控制項： [InkEdit](inkedit-control.md) 和 [InkPicture](inkpicture-control.md)，可讓您輕鬆地將筆跡和手寫辨識新增到 Tablet PC 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="4aa1d-105">InkEdit 控制項具有 [managed](/previous-versions/ms835842(v=msdn.10))、 [ActiveX](inkedit-control-reference.md) 和 Win32 版本，而 InkPicture 只有 managed [InkPicture](/previous-versions/ms583740(v=vs.100)) 和 [activex](inkpicture-control-reference.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="4aa1d-106">控制項之間的主要差異在於資料的儲存方式。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="4aa1d-107">[InkEdit](inkedit-control.md)控制項會依預設將筆墨儲存為文字，而[InkPicture](inkpicture-control.md)則會將筆墨儲存為筆跡。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="4aa1d-108">[InkEdit](inkedit-control.md)控制項適用于透過手寫辨識的文字輸入。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="4aa1d-109">[InkPicture](inkpicture-control.md) 適用于批註 (例如，標示簡報投影片或其他圖片) 。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="4aa1d-110">在 managed 程式碼中，在與表單主執行緒相同的執行緒中建立筆墨控制項。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="4aa1d-111">如果在不同的執行緒中建立 [InkEdit](inkedit-control.md) 或 [InkPicture](inkpicture-control.md) 控制項，則您的應用程式可能無法正確回應。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="4aa1d-112">建立筆墨控制項之前，您應該明確地將執行緒模型變更為單一線程的單元 (STA) 。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="4aa1d-113">這會導致在主執行緒上建立控制項。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="4aa1d-114">您可以使用下列 Managed c + + 程式碼來明確設定執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="4aa1d-115">您可以使用下列程式碼，在 C 中執行相同的動作 \# 。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="4aa1d-116">在 managed 程式碼中，若要避免記憶體流失，您必須在控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="4aa1d-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="4aa1d-117">下列各節說明筆墨控制項，以及在應用程式中使用筆墨控制項的方式：</span><span class="sxs-lookup"><span data-stu-id="4aa1d-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="4aa1d-118">將筆墨控制項新增至專案</span><span class="sxs-lookup"><span data-stu-id="4aa1d-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="4aa1d-119">InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="4aa1d-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="4aa1d-120">InkPicture 控制項</span><span class="sxs-lookup"><span data-stu-id="4aa1d-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
