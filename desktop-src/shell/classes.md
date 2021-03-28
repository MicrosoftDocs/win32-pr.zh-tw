---
description: 本節說明 Windows Shell 類別。
ms.assetid: 3b9d876c-32a9-429f-9605-efcc4a1c1570
title: Shell 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bc306215d6ecdc9c60ff6aa5bc70e85ad27b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991090"
---
# <a name="shell-classes"></a><span data-ttu-id="50516-103">Shell 類別</span><span class="sxs-lookup"><span data-stu-id="50516-103">Shell Classes</span></span>

<span data-ttu-id="50516-104">本節說明 Windows Shell 類別。</span><span class="sxs-lookup"><span data-stu-id="50516-104">This section describes the Windows Shell classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50516-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="50516-105">In this section</span></span>



| <span data-ttu-id="50516-106">主題</span><span class="sxs-lookup"><span data-stu-id="50516-106">Topic</span></span>                                                               | <span data-ttu-id="50516-107">描述</span><span class="sxs-lookup"><span data-stu-id="50516-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50516-108">[**CCscSearchApiInterface**](/previous-versions/windows/desktop/legacy/cc448312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50516-108">[**CCscSearchApiInterface**](/previous-versions/windows/desktop/legacy/cc448312(v=vs.85))</span></span><br/> | <span data-ttu-id="50516-109">公開與 CSC (用戶端快取互動的方法，也稱為離線檔案) 搜尋 API 程式庫。</span><span class="sxs-lookup"><span data-stu-id="50516-109">Exposes methods for interacting with the CSC (Client Side Caching, also known as Offline Files) search API library.</span></span><br/>                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="50516-110">**CFolderItems**</span><span class="sxs-lookup"><span data-stu-id="50516-110">**CFolderItems**</span></span>](class-cfolderitems-class.md)<br/>         | <span data-ttu-id="50516-111">[**CFolderItems**](class-cfolderitems-class.md) 是 [**FolderItems**](folderitems.md)的集合。</span><span class="sxs-lookup"><span data-stu-id="50516-111">[**CFolderItems**](class-cfolderitems-class.md) is a collection of [**FolderItems**](folderitems.md).</span></span> <span data-ttu-id="50516-112">它會執行下列介面： [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)、 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)、 [**FolderItems3**](folderitems3-object.md)、 [**IObjectSafety**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768224(v=vs.85))、 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。</span><span class="sxs-lookup"><span data-stu-id="50516-112">It implements the following interfaces: [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**FolderItems3**](folderitems3-object.md), [**IObjectSafety**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768224(v=vs.85)), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span><br/> |
| [<span data-ttu-id="50516-113">**CFolderItemsFDF**</span><span class="sxs-lookup"><span data-stu-id="50516-113">**CFolderItemsFDF**</span></span>](class-cfolderitemsfdf-class.md)<br/>   | <span data-ttu-id="50516-114">[**CFolderItemsFDF**](class-cfolderitemsfdf-class.md) 是 [**FolderItems**](folderitems.md)的集合。</span><span class="sxs-lookup"><span data-stu-id="50516-114">[**CFolderItemsFDF**](class-cfolderitemsfdf-class.md) is a collection of [**FolderItems**](folderitems.md).</span></span> <span data-ttu-id="50516-115">它會實 [**IInsertItem**](/windows/desktop/api/Shobjidl/nn-shobjidl-iinsertitem) 介面。</span><span class="sxs-lookup"><span data-stu-id="50516-115">It implements the [**IInsertItem**](/windows/desktop/api/Shobjidl/nn-shobjidl-iinsertitem) interface.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="50516-116">**CItemIDFactory**</span><span class="sxs-lookup"><span data-stu-id="50516-116">**CItemIDFactory**</span></span>](/windows/desktop/api/shidfact/nl-shidfact-citemidfactory)<br/>                 | <span data-ttu-id="50516-117">公開與 Shell 資料來源互動的方法。</span><span class="sxs-lookup"><span data-stu-id="50516-117">Exposes methods for interacting with Shell data sources.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="50516-118">**VirtualDesktopManager**</span><span class="sxs-lookup"><span data-stu-id="50516-118">**VirtualDesktopManager**</span></span>](virtualdesktopmanager.md)<br/>   | <span data-ttu-id="50516-119">[**VirtualDesktopManager**](virtualdesktopmanager.md) 會實 [**IVirtualDesktopManager**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="50516-119">[**VirtualDesktopManager**](virtualdesktopmanager.md) implements the [**IVirtualDesktopManager**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager) interface.</span></span><br/>                                                                                                                                                                                                                                                         |



 

 

 
