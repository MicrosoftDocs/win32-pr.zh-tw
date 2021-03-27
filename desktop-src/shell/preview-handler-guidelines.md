---
description: 當您提供預覽時，應遵循下列指導方針。
title: 預覽處理常式指導方針
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850036"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="a7a31-103">預覽處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="a7a31-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="a7a31-104">當您提供預覽時，應遵循下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="a7a31-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="a7a31-105">預覽版應包含基本的 UI，只是預覽。</span><span class="sxs-lookup"><span data-stu-id="a7a31-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="a7a31-106">它應該只顯示檔案內容。</span><span class="sxs-lookup"><span data-stu-id="a7a31-106">It should display only the file content.</span></span> <span data-ttu-id="a7a31-107">它不應該顯示對話方塊、啟動顯示畫面、工具列或工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a7a31-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="a7a31-108">讀取窗格通常會與搜尋搭配使用，以快速識別檔案。</span><span class="sxs-lookup"><span data-stu-id="a7a31-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="a7a31-109">Clutters [閱讀] 窗格或從檔案內容會使或在預覽顯示期間造成延遲的任何事，都應予以避免。</span><span class="sxs-lookup"><span data-stu-id="a7a31-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="a7a31-110">預覽版應可讓使用者在檔中流覽。</span><span class="sxs-lookup"><span data-stu-id="a7a31-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="a7a31-111">使用者也應該可以選取和複製文字。</span><span class="sxs-lookup"><span data-stu-id="a7a31-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="a7a31-112">預覽應該不需要海量儲存體，應該耗用最少量的資源，而且應該要有快速的啟動時間。</span><span class="sxs-lookup"><span data-stu-id="a7a31-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="a7a31-113">基於安全性和隱私權目的，應封鎖正在預覽的檔案中的所有腳本和宏。</span><span class="sxs-lookup"><span data-stu-id="a7a31-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="a7a31-114">預覽版應該支援應用程式所支援的導覽和選取的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="a7a31-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="a7a31-115">當您按一下滑鼠右鍵時，也應該會顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="a7a31-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="a7a31-116">當檔案顯示為預覽時，預覽不應鎖定檔案本身。</span><span class="sxs-lookup"><span data-stu-id="a7a31-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="a7a31-117">您可以同時在其相關聯的應用程式中預覽及開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7a31-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7a31-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7a31-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7a31-119">預覽處理常式和 Shell 預覽主機</span><span class="sxs-lookup"><span data-stu-id="a7a31-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="a7a31-120">建立預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="a7a31-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



