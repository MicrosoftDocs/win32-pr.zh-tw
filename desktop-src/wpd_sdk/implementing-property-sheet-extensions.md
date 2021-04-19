---
description: 執行屬性工作表延伸模組
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: 執行屬性工作表延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987824"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="77fb0-103">執行屬性工作表延伸模組</span><span class="sxs-lookup"><span data-stu-id="77fb0-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="77fb0-104">WPD 命名空間延伸模組支援可擴充的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="77fb0-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="77fb0-105">當使用者以滑鼠右鍵按一下某個物件（例如檔案或資料夾）並選取 [ **屬性**] 時，就會出現這些屬性對話方塊。</span><span class="sxs-lookup"><span data-stu-id="77fb0-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="77fb0-106">某些 WPD 應用程式會利用這些可延伸的屬性工作表來顯示裝置端內容 (的屬性，或是位於裝置) 的物件。</span><span class="sxs-lookup"><span data-stu-id="77fb0-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="77fb0-107">下表所述的介面支援可延伸的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="77fb0-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="77fb0-108">如需這些介面的詳細資訊，請參閱 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="77fb0-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="77fb0-109">介面</span><span class="sxs-lookup"><span data-stu-id="77fb0-109">Interface</span></span>           | <span data-ttu-id="77fb0-110">描述</span><span class="sxs-lookup"><span data-stu-id="77fb0-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="77fb0-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="77fb0-111">IDataObject</span></span>         | <span data-ttu-id="77fb0-112">用來將內容功能表的 PIDL 陣列傳遞至內容功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="77fb0-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="77fb0-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="77fb0-113">IPropertySetStorage</span></span> | <span data-ttu-id="77fb0-114">這個介面是用來取得指定物件的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="77fb0-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="77fb0-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="77fb0-115">IPropertyStorage</span></span>    | <span data-ttu-id="77fb0-116">這個介面也用來取出指定物件的 WPD 屬性。</span><span class="sxs-lookup"><span data-stu-id="77fb0-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="77fb0-117">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="77fb0-117">IShellExtInit</span></span>       | <span data-ttu-id="77fb0-118">初始化內容功能表的 Windows Vista Shell 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77fb0-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="77fb0-119">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="77fb0-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="77fb0-120">支援加入屬性工作表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="77fb0-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="77fb0-121">WPD 的屬性工作表會像 Windows Vista 中的任何其他屬性工作表一樣執行。</span><span class="sxs-lookup"><span data-stu-id="77fb0-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="77fb0-122">如果您已經執行屬性工作表處理常式，您可以修改現有的程式碼，使其支援裝置端的內容。</span><span class="sxs-lookup"><span data-stu-id="77fb0-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="77fb0-123">如果您從未建立內容功能表處理常式，請參閱 Windows SDK 中的建立屬性工作表處理常式主題。</span><span class="sxs-lookup"><span data-stu-id="77fb0-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="77fb0-124">WPD 屬性工作表處理常式與任何其他處理常式不同的點是在處理常式註冊和裝置端內容支援。</span><span class="sxs-lookup"><span data-stu-id="77fb0-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



