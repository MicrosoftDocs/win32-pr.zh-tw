---
title: IADs 和 IDirectoryObject 介面
description: ADSI 用戶端會使用兩個 COM 介面 IADs 或 IDirectoryObject 中的其中一個來管理和操作目錄服務物件。
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI，關於
- IDirectoryObject ADSI，關於
- ADSI ADSI、using、IADs 和 IDirectoryObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842736"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a><span data-ttu-id="3c3df-106">IADs 和 IDirectoryObject 介面</span><span class="sxs-lookup"><span data-stu-id="3c3df-106">The IADs and IDirectoryObject Interfaces</span></span>

<span data-ttu-id="3c3df-107">ADSI 用戶端會使用兩個 COM 介面的其中一個來管理和操作目錄服務物件： [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 或 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)。</span><span class="sxs-lookup"><span data-stu-id="3c3df-107">ADSI clients manage and manipulate directory service objects by using one of two COM interfaces: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="3c3df-108">**IADs** 是一個 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面，可供晚期繫結的用戶端使用，例如以 Microsoft Visual Basic、JAVA 和各種指令碼語言撰寫的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3c3df-108">**IADs** is an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface intended for use by late-bound clients such as those written in Microsoft Visual Basic, Java, and various scripting languages.</span></span> <span data-ttu-id="3c3df-109">**IDirectoryObject** 是一種 vtable 介面，可讓您直接存取以 C 和 c + + 撰寫的早期繫結用戶端物件。</span><span class="sxs-lookup"><span data-stu-id="3c3df-109">**IDirectoryObject** is a vtable interface that provides direct access to objects by early bound clients such as those written in C and C++.</span></span>

<span data-ttu-id="3c3df-110">每個 ADSI 物件都必須同時執行 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 和 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)。</span><span class="sxs-lookup"><span data-stu-id="3c3df-110">Each ADSI object must implement both [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="3c3df-111">以 C 或 c + + 等語言撰寫的 ADSI 用戶端（可以直接存取 vtable）可以使用任一種介面，但不能同時在相同的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="3c3df-111">ADSI clients written in languages such as C or C++, which are able to directly access vtables, can use either interface, but not both in the same application.</span></span> <span data-ttu-id="3c3df-112">以 Visual Basic 或 JAVA 撰寫的 ADSI 用戶端僅限使用 **IADs**。</span><span class="sxs-lookup"><span data-stu-id="3c3df-112">ADSI clients written in Visual Basic or Java are limited to using **IADs**.</span></span>

<span data-ttu-id="3c3df-113">[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面可讓晚期繫結用戶端利用 ADSI 物件模型的固有維護功能。</span><span class="sxs-lookup"><span data-stu-id="3c3df-113">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface enables late-bound clients to take advantage of the inherent housekeeping features of the ADSI object model.</span></span> <span data-ttu-id="3c3df-114">這些功能包括屬性快取，可讓用戶端讀取和寫入屬性，而不需要透過網路進行每次呼叫。</span><span class="sxs-lookup"><span data-stu-id="3c3df-114">Among these features is the property cache, which enables clients to read and write properties without going over the wire for each call.</span></span> <span data-ttu-id="3c3df-115">此外，用戶端應用程式也能充分利用功能強大的 UI 和 ActiveX 控制項程式庫，以及更簡單的程式設計樣式。</span><span class="sxs-lookup"><span data-stu-id="3c3df-115">In addition, client applications gain the use of powerful UI and ActiveX control libraries and a simpler style of programming.</span></span> <span data-ttu-id="3c3df-116">在傳回時，晚期繫結用戶端必須使用 **VARIANT** 資料類型，這會使用 ADSI 所提供的更豐富原生資料類型來排除。</span><span class="sxs-lookup"><span data-stu-id="3c3df-116">In return, late-bound clients must use the **VARIANT** data type, which precludes using the richer native data types provided by ADSI.</span></span>

<span data-ttu-id="3c3df-117">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面讓較早系結的用戶端能夠充分利用原生目錄服務的資料類型，但在上述的成本上，使用屬性快取的效能會稍微低一點。</span><span class="sxs-lookup"><span data-stu-id="3c3df-117">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface enables early bound clients to take full advantage of native directory-service data types at the cost of foregoing a slight performance advantage from using the property cache.</span></span> <span data-ttu-id="3c3df-118">**IDirectoryObject** 介面會透過單一要求（而不是透過個別的 **get** 和 **put** 呼叫），提供物件屬性的直接線上存取。</span><span class="sxs-lookup"><span data-stu-id="3c3df-118">In return, the **IDirectoryObject** interface provides direct, on-the-wire access to object properties through a single request, rather than through individual **get** and **put** calls.</span></span>

 

 