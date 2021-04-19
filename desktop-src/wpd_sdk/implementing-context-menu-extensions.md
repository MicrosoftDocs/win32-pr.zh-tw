---
description: 執行內容功能表延伸模組
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: 執行內容功能表延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997530"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="a273e-103">執行內容功能表延伸模組</span><span class="sxs-lookup"><span data-stu-id="a273e-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="a273e-104">WPD 命名空間延伸模組支援可擴充的內容 (或快捷方式) 功能表。</span><span class="sxs-lookup"><span data-stu-id="a273e-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="a273e-105">這些是使用者以滑鼠右鍵按一下某個物件（例如檔案或資料夾）時所顯示的功能表。</span><span class="sxs-lookup"><span data-stu-id="a273e-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="a273e-106">某些 WPD 應用程式會利用這些可延伸的功能表，來支援裝置端內容 (或位於裝置) 上的物件的作業。</span><span class="sxs-lookup"><span data-stu-id="a273e-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="a273e-107">下表所述的介面支援可擴充的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="a273e-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="a273e-108">如需這些介面的詳細資訊，請參閱 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="a273e-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="a273e-109">介面</span><span class="sxs-lookup"><span data-stu-id="a273e-109">Interface</span></span>           | <span data-ttu-id="a273e-110">描述</span><span class="sxs-lookup"><span data-stu-id="a273e-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a273e-111">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="a273e-111">IContextMenu</span></span>        | <span data-ttu-id="a273e-112">Windows Vista Shell 會呼叫此介面中的方法，以建立新的內容功能表，或將其與指定的物件合併。</span><span class="sxs-lookup"><span data-stu-id="a273e-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="a273e-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="a273e-113">IDataObject</span></span>         | <span data-ttu-id="a273e-114">用來將內容功能表的 PIDL 陣列傳遞至內容功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="a273e-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="a273e-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="a273e-115">IPropertySetStorage</span></span> | <span data-ttu-id="a273e-116">這個介面是用來取得指定物件的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="a273e-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="a273e-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="a273e-117">IPropertyStorage</span></span>    | <span data-ttu-id="a273e-118">這個介面也用來取出指定物件的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="a273e-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="a273e-119">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="a273e-119">IShellExtInit</span></span>       | <span data-ttu-id="a273e-120">初始化內容功能表的 Windows Vista Shell 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="a273e-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="a273e-121">IStream</span><span class="sxs-lookup"><span data-stu-id="a273e-121">IStream</span></span>             | <span data-ttu-id="a273e-122">提供。</span><span class="sxs-lookup"><span data-stu-id="a273e-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="a273e-123">WPD 的內容功能表會像 Windows Vista 中的任何其他內容功能表一樣執行。</span><span class="sxs-lookup"><span data-stu-id="a273e-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="a273e-124">如果您已經執行內容功能表處理常式，您可以修改現有的程式碼，使其支援裝置端的內容。</span><span class="sxs-lookup"><span data-stu-id="a273e-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="a273e-125">如果您從未建立內容功能表處理常式，請參閱 Windows SDK 中的建立內容功能表處理常式主題。</span><span class="sxs-lookup"><span data-stu-id="a273e-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="a273e-126">WPD 內容功能表處理常式與任何其他處理常式不同的點是在處理常式註冊和裝置端內容支援。</span><span class="sxs-lookup"><span data-stu-id="a273e-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



