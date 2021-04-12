---
title: 指標標記
description: 指標標記會識別只能存在於作用中或正在執行狀態的物件。 這與其他標記類別不同，後者會識別可以存在於被動或主動狀態的物件。
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104374194"
---
# <a name="pointer-monikers"></a><span data-ttu-id="94cdc-104">指標標記</span><span class="sxs-lookup"><span data-stu-id="94cdc-104">Pointer Monikers</span></span>

<span data-ttu-id="94cdc-105">*指標標記* 會識別只能存在於作用中或正在執行狀態的物件。</span><span class="sxs-lookup"><span data-stu-id="94cdc-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="94cdc-106">這與其他標記類別不同，後者會識別可以存在於被動或主動狀態的物件。</span><span class="sxs-lookup"><span data-stu-id="94cdc-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="94cdc-107">例如，假設應用程式有一個沒有持續表示的物件。</span><span class="sxs-lookup"><span data-stu-id="94cdc-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="94cdc-108">一般來說，如果您的應用程式用戶端需要存取該物件，您就可以直接將物件的指標傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="94cdc-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="94cdc-109">不過，假設您的用戶端預期會有一個名字標記。</span><span class="sxs-lookup"><span data-stu-id="94cdc-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="94cdc-110">無法使用檔案的標記來識別物件，因為它不會儲存在檔案中，也不會儲存在專案的標記中，因為它不包含在另一個物件中。</span><span class="sxs-lookup"><span data-stu-id="94cdc-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="94cdc-111">相反地，您的應用程式可以建立指標標記，也就是只在內部包含指標的標記，並將其傳遞至用戶端。</span><span class="sxs-lookup"><span data-stu-id="94cdc-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="94cdc-112">用戶端可以將此標記視為任何其他物件。</span><span class="sxs-lookup"><span data-stu-id="94cdc-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="94cdc-113">不過，當用戶端在指標名字標記上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 時，標記代碼不會檢查執行中的物件資料表 (的 ROT) 或從儲存體載入任何內容。</span><span class="sxs-lookup"><span data-stu-id="94cdc-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="94cdc-114">相反地，標記程式碼只會在儲存于標記內的指標上呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="94cdc-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="94cdc-115">指標標記可讓只存在於作用中或執行中狀態的物件參與標記作業，並由標記用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="94cdc-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="94cdc-116">指標名字和其他標記類別之間有一個重要的差異，就是無法將指標標記儲存至持續性儲存區。</span><span class="sxs-lookup"><span data-stu-id="94cdc-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="94cdc-117">如果您這樣做，呼叫 [**IMoniker：： Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) 方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="94cdc-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="94cdc-118">這表示指標標記只有在特殊的情況下才有用。</span><span class="sxs-lookup"><span data-stu-id="94cdc-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="94cdc-119">如果您需要使用指標標記，可以使用 [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) 函數。</span><span class="sxs-lookup"><span data-stu-id="94cdc-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94cdc-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="94cdc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94cdc-121">反標記</span><span class="sxs-lookup"><span data-stu-id="94cdc-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="94cdc-122">類別名字標記</span><span class="sxs-lookup"><span data-stu-id="94cdc-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="94cdc-123">複合的名字</span><span class="sxs-lookup"><span data-stu-id="94cdc-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="94cdc-124">檔案名字</span><span class="sxs-lookup"><span data-stu-id="94cdc-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="94cdc-125">專案的名字</span><span class="sxs-lookup"><span data-stu-id="94cdc-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




