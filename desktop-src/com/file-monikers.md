---
title: 檔案名字
description: 檔案名字
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300472"
---
# <a name="file-monikers"></a><span data-ttu-id="72cb8-103">檔案名字</span><span class="sxs-lookup"><span data-stu-id="72cb8-103">File Monikers</span></span>

<span data-ttu-id="72cb8-104">檔案 *名字* 標記是最簡單的標記類別。</span><span class="sxs-lookup"><span data-stu-id="72cb8-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="72cb8-105">檔案標記可以用來識別儲存在它自己的檔案中的任何物件。</span><span class="sxs-lookup"><span data-stu-id="72cb8-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="72cb8-106">檔案的標記可做為原生檔案系統指派給檔案之路徑名稱的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="72cb8-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="72cb8-107">針對這個標記呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 會導致這個物件啟動，然後傳回物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="72cb8-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="72cb8-108">以標記命名的物件來源必須提供 [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) 介面的實作為支援系結檔案的標記。</span><span class="sxs-lookup"><span data-stu-id="72cb8-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="72cb8-109">檔案副檔名可以是完整或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="72cb8-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="72cb8-110">例如，儲存為 file C： WorkMySheet.xls 之試算表物件的檔案標記 \\ \\ 會包含與該路徑名稱相等的資訊。</span><span class="sxs-lookup"><span data-stu-id="72cb8-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="72cb8-111">但是，此標記不一定是由相同的字串所組成。</span><span class="sxs-lookup"><span data-stu-id="72cb8-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="72cb8-112">字串只是其 *displayÂ名稱*，表示對使用者有意義的名字標記內容。</span><span class="sxs-lookup"><span data-stu-id="72cb8-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="72cb8-113">顯示名稱（可透過 [**IMoniker：： GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) 方法取得）只會在向使用者顯示標記時使用。</span><span class="sxs-lookup"><span data-stu-id="72cb8-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="72cb8-114">這個方法會取得任何標記類別的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="72cb8-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="72cb8-115">就內部而言，此標記可能會以較有效率的格式來儲存相同的資訊，以執行「名字」作業，但對使用者來說不具意義。</span><span class="sxs-lookup"><span data-stu-id="72cb8-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="72cb8-116">然後，當這個相同的物件透過呼叫 [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 方法系結時，就可能會將該檔案載入試算表中，以啟用該物件。</span><span class="sxs-lookup"><span data-stu-id="72cb8-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="72cb8-117">OLE 提供 helper 函式 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) 的 helper 函式，它會建立檔案的標記物件，並將其指標傳回給提供者。</span><span class="sxs-lookup"><span data-stu-id="72cb8-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72cb8-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="72cb8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72cb8-119">反標記</span><span class="sxs-lookup"><span data-stu-id="72cb8-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="72cb8-120">類別名字標記</span><span class="sxs-lookup"><span data-stu-id="72cb8-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="72cb8-121">複合的名字</span><span class="sxs-lookup"><span data-stu-id="72cb8-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="72cb8-122">專案的名字</span><span class="sxs-lookup"><span data-stu-id="72cb8-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="72cb8-123">指標標記</span><span class="sxs-lookup"><span data-stu-id="72cb8-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




