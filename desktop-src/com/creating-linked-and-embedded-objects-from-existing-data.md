---
title: 從現有資料建立連結和內嵌物件
description: 從現有資料建立連結和內嵌物件
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675711"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="9fdfc-103">從現有資料建立連結和內嵌物件</span><span class="sxs-lookup"><span data-stu-id="9fdfc-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="9fdfc-104">使用者通常會使用剪貼簿或拖放將資料物件從其伺服器應用程式複製到使用者的容器應用程式，以組合複合檔案。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="9fdfc-105">使用支援 OLE 的應用程式，使用者可以從伺服器或容器起始傳送。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="9fdfc-106">例如，伺服器可以將資料複製到伺服器應用程式中的剪貼簿，然後切換至容器應用程式，並選擇 [貼上特殊/内嵌物件] 或 [對應的功能表] 命令，從選取的資料建立新的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="9fdfc-107">或者，使用者可以將資料從一個應用程式拖曳到另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="9fdfc-108">此程式類似于建立連結化物件。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="9fdfc-109">同時做為 OLE 伺服器和容器使用的應用程式可以使用自己的資料選取範圍，在相同檔中的新位置建立內嵌或連結的物件。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="9fdfc-110">OLE 伺服器和容器應用程式之間的資料傳輸是以統一的資料傳輸為基礎，如 [資料傳輸](data-transfer.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="9fdfc-111">OLE 伺服器和物件處理常式會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ，以便使用剪貼簿或拖放功能，將其資料提供給傳輸。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="9fdfc-112">OLE 物件支援所有常用的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="9fdfc-113">此外，它們支援六種剪貼簿格式，可支援從選取的資料物件建立連結和內嵌的物件。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="9fdfc-114">OLE 剪貼簿格式描述在 OLE 容器中卸載或貼上的資料物件，會成為內嵌或連結的複合檔案物件。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="9fdfc-115">資料物件會將這些格式呈現給容器應用程式，以將其精確度視為資料的描述。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="9fdfc-116">換句話說，物件會先顯示最能代表它的格式，然後是下一個最佳格式，依此類推。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="9fdfc-117">這種刻意的順序鼓勵容器應用程式使用最可能的格式。</span><span class="sxs-lookup"><span data-stu-id="9fdfc-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fdfc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fdfc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fdfc-119">複合檔案</span><span class="sxs-lookup"><span data-stu-id="9fdfc-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="9fdfc-120">資料轉送</span><span class="sxs-lookup"><span data-stu-id="9fdfc-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




