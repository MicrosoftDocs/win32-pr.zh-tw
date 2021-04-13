---
title: 類別名字標記
description: 雖然類別通常會直接以 Clsid （例如 CoCreateInstance 或 CoGetClassObject）的 Clsid 來識別，但是類別現在也可以使用稱為類別標記的標記來識別。
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311175"
---
# <a name="class-monikers"></a><span data-ttu-id="ed2cc-103">類別名字標記</span><span class="sxs-lookup"><span data-stu-id="ed2cc-103">Class Monikers</span></span>

<span data-ttu-id="ed2cc-104">雖然類別通常會直接以 Clsid （例如 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)）的 clsid 來識別，但是類別現在也可以使用稱為 *類別標記* 的標記來識別。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="ed2cc-105">類別標記系結至其所建立之類別的類別物件。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="ed2cc-106">找出具有標記之類別的能力，可支援無法使用的實用作業。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="ed2cc-107">例如，檔案的標記通常只支援將 rich binding 系結至與所參考之檔案類別相關聯的類別;Excel 檔案的標記會系結至 Excel 物件的實例，而 GIF 影像的標記會系結至目前註冊之 GIF 處理常式的實例。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="ed2cc-108">類別的「標記」（class）可讓您指定要用來透過包含檔案標記的組合來操作檔案的類別。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="ed2cc-109">以標記撰寫至 Excel 檔案的3D 圖表類別類別的類別標記會產生一個會系結至3D 圖表物件實例的標記，並使用 Excel 檔案的內容來初始化物件。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="ed2cc-110">因此，類別名字標記最適合用來與其他類型的專案組合（例如檔案的副檔名或專案的名字標記）組合。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="ed2cc-111">類別的標記也可以撰寫至支援系結至 [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) 介面的名字標記右邊。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="ed2cc-112">以這種方式撰寫時， **IClassActivator** 只會透過 [**IClassActivator：： GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject)提供類別物件和類別實例的存取權。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="ed2cc-113">類別的標記可透過 [**IMoniker：： IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker)來識別，其會傳回 \_ *pdwMksys* 中的 MKSYS CLASSMONIKER。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="ed2cc-114">程式設計人員通常會使用 [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) 函式或透過 [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname)來建立類別標記。</span><span class="sxs-lookup"><span data-stu-id="ed2cc-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="ed2cc-115"> (參閱 [**IMoniker：:P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) ，以取得詳細資料。 ) </span><span class="sxs-lookup"><span data-stu-id="ed2cc-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed2cc-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed2cc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed2cc-117">反標記</span><span class="sxs-lookup"><span data-stu-id="ed2cc-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="ed2cc-118">複合的名字</span><span class="sxs-lookup"><span data-stu-id="ed2cc-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="ed2cc-119">檔案名字</span><span class="sxs-lookup"><span data-stu-id="ed2cc-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="ed2cc-120">專案的名字</span><span class="sxs-lookup"><span data-stu-id="ed2cc-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="ed2cc-121">指標標記</span><span class="sxs-lookup"><span data-stu-id="ed2cc-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




