---
title: COM 物件和介面
description: COM 物件和介面
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671391"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="04333-103">COM 物件和介面</span><span class="sxs-lookup"><span data-stu-id="04333-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="04333-104">COM 是一種技術，可讓物件在進程和電腦界限之間進行互動，就像在單一進程內一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="04333-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="04333-105">COM 可透過指定操作與物件相關聯之資料的唯一方法，來達成此目的。 </span><span class="sxs-lookup"><span data-stu-id="04333-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="04333-106">本檔中使用此詞彙時，是指與物件相關聯之 COM 二進位相容介面的程式碼中的實作為。</span><span class="sxs-lookup"><span data-stu-id="04333-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="04333-107">COM 使用 word *介面* ，與通常用於 Visual C++ 程式設計的意義不同。</span><span class="sxs-lookup"><span data-stu-id="04333-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="04333-108">C + + 介面指的是類別支援的所有函式，而物件的用戶端可以呼叫來與其互動。</span><span class="sxs-lookup"><span data-stu-id="04333-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="04333-109">COM 介面指的是 COM 類別所執行的一組預先定義的相關函式，但特定介面不一定代表該類別支援的所有函式。</span><span class="sxs-lookup"><span data-stu-id="04333-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="04333-110">參考執行介面的物件表示物件使用的程式碼會 *執行* 介面的每個方法，並將這些函式的 com 二進位相容指標提供給 com 程式庫。</span><span class="sxs-lookup"><span data-stu-id="04333-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="04333-111">然後，COM 會將這些函式提供給要求介面指標的任何用戶端使用，不論用戶端是在執行這些函式的進程內部或外部。</span><span class="sxs-lookup"><span data-stu-id="04333-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="04333-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="04333-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="04333-113">介面和介面的實現</span><span class="sxs-lookup"><span data-stu-id="04333-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="04333-114">介面指標和介面</span><span class="sxs-lookup"><span data-stu-id="04333-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="04333-115">IUnknown 和介面繼承</span><span class="sxs-lookup"><span data-stu-id="04333-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="04333-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="04333-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04333-117">介面</span><span class="sxs-lookup"><span data-stu-id="04333-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




