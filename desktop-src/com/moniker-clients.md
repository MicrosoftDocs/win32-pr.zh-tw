---
title: 標記用戶端
description: 「名字」用戶端必須透過取得名字標記來開始，而且有數種方式可讓「標記」用戶端取得標記。
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969835"
---
# <a name="moniker-clients"></a><span data-ttu-id="ec893-103">標記用戶端</span><span class="sxs-lookup"><span data-stu-id="ec893-103">Moniker Clients</span></span>

<span data-ttu-id="ec893-104">「名字」用戶端必須透過取得名字標記來開始，而且有數種方式可讓「標記」用戶端取得標記。</span><span class="sxs-lookup"><span data-stu-id="ec893-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="ec893-105">例如，在 OLE 複合檔案中，當使用者建立連結專案 (使用 [ **插入物件** ] 對話方塊、剪貼簿或拖放) 時，會將標記內嵌為連結專案的一部分。</span><span class="sxs-lookup"><span data-stu-id="ec893-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="ec893-106">在這種情況下，程式設計人員與名字的聯繫性最短。</span><span class="sxs-lookup"><span data-stu-id="ec893-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="ec893-107">以程式設計的方式，如果您有一個介面指標指向可執行 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件，您可以使用該介面指標來取得標記，並在定義的其他介面上提供方法來傳回名字標記。</span><span class="sxs-lookup"><span data-stu-id="ec893-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="ec893-108">有不同類型的標記，用來識別不同類型的物件，但對標記用戶端而言，所有的標記看起來都一樣。</span><span class="sxs-lookup"><span data-stu-id="ec893-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="ec893-109">標記用戶端只會在標記上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ，並取得標記所識別之物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="ec893-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="ec893-110">無論是否將物件識別為與整個試算表一樣大的物件，或以試算表內的單一資料格作為小者，呼叫 **BindToObject** 將會傳回該物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ec893-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="ec893-111">如果物件已在執行中， **BindToObject** 會在記憶體中找到它。</span><span class="sxs-lookup"><span data-stu-id="ec893-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="ec893-112">如果物件是以被動的狀態儲存在磁片上， **BindToObject** 將會找出該物件的伺服器、執行伺服器，然後讓伺服器將物件帶到執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="ec893-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="ec893-113">所有的系結程式詳細資料都不會從 [標記用戶端] 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="ec893-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="ec893-114">因此，針對標記用戶端，使用標記非常簡單。</span><span class="sxs-lookup"><span data-stu-id="ec893-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec893-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec893-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec893-116">標記提供者</span><span class="sxs-lookup"><span data-stu-id="ec893-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="ec893-117">OLE 標記執行</span><span class="sxs-lookup"><span data-stu-id="ec893-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




