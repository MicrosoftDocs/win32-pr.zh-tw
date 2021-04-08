---
title: 無視窗的 Rich Edit 控制項
description: 本章節包含與無視窗 rich edit 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021052"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="61025-103">無視窗的 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="61025-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="61025-104">本章節包含與無視窗 rich edit 控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="61025-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="61025-105">元件物件模型 (COM) 會定義一組介面，以支援無視窗的物件。</span><span class="sxs-lookup"><span data-stu-id="61025-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="61025-106">無視窗物件可以輸入就地作用中狀態，而不需要自己的視窗，而是使用其容器的視窗。</span><span class="sxs-lookup"><span data-stu-id="61025-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="61025-107">因此，無視窗物件會使用較少的系統資源，並透過更快速的啟用和停用提供更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="61025-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="61025-108">此外，無視窗的物件可以是非矩形且透明的。</span><span class="sxs-lookup"><span data-stu-id="61025-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="61025-109">概觀</span><span class="sxs-lookup"><span data-stu-id="61025-109">Overviews</span></span>



| <span data-ttu-id="61025-110">主題</span><span class="sxs-lookup"><span data-stu-id="61025-110">Topic</span></span>                                                                          | <span data-ttu-id="61025-111">目錄</span><span class="sxs-lookup"><span data-stu-id="61025-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61025-112">關於無視窗的 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="61025-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="61025-113">無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供 [豐富編輯控制項](rich-edit-controls.md) 的功能，而不需提供視窗。</span><span class="sxs-lookup"><span data-stu-id="61025-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="61025-114">函式</span><span class="sxs-lookup"><span data-stu-id="61025-114">Functions</span></span>



| <span data-ttu-id="61025-115">主題</span><span class="sxs-lookup"><span data-stu-id="61025-115">Topic</span></span>                                            | <span data-ttu-id="61025-116">目錄</span><span class="sxs-lookup"><span data-stu-id="61025-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61025-117">**CreateTextServices**</span><span class="sxs-lookup"><span data-stu-id="61025-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="61025-118">[**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices)函式會建立文字服務物件的實例。</span><span class="sxs-lookup"><span data-stu-id="61025-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="61025-119">文字服務物件支援各種不同的介面，包括 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 Text 物件模型 (TOM) 。</span><span class="sxs-lookup"><span data-stu-id="61025-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="61025-120">介面</span><span class="sxs-lookup"><span data-stu-id="61025-120">Interfaces</span></span>



| <span data-ttu-id="61025-121">主題</span><span class="sxs-lookup"><span data-stu-id="61025-121">Topic</span></span>                                  | <span data-ttu-id="61025-122">目錄</span><span class="sxs-lookup"><span data-stu-id="61025-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61025-123">**ITextHost**</span><span class="sxs-lookup"><span data-stu-id="61025-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="61025-124">[**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)介面是由文字服務物件用來取得文字主機服務。</span><span class="sxs-lookup"><span data-stu-id="61025-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="61025-125">**ITextServices**</span><span class="sxs-lookup"><span data-stu-id="61025-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="61025-126">擴充 TOM 以提供無視窗操作的額外功能。</span><span class="sxs-lookup"><span data-stu-id="61025-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





