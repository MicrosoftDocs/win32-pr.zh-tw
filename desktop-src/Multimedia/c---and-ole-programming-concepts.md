---
title: C + + 和 OLE 程式設計概念
description: C + + 和 OLE 程式設計概念
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840828"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="ba6b5-103">C + + 和 OLE 程式設計概念</span><span class="sxs-lookup"><span data-stu-id="ba6b5-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="ba6b5-104">Windows 隨附的檔案和資料流程處理常式使用物件導向設計來提升標準介面並共用功能。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="ba6b5-105">這些處理常式是以 c + + 撰寫，並使用 OLE 元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="ba6b5-106">您可以使用 C 或 c + + 開發系統開發自訂處理常式;不過，強烈建議使用 c + +，因為它提供更簡單且更簡單的方法來執行處理常式。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="ba6b5-107">使用 c + +，您可以將資料明確定義為物件，也可以將運算元據的函式與物件的成員函式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="ba6b5-108">本節將識別並簡短摘要說明 c + + 的重要概念，以及適用于設計和執行檔案和串流處理常式的 OLE 元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="ba6b5-109">有許多關於 c + + 程式設計的書籍，您可以參考這些書籍以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="ba6b5-110">如需 OLE 的詳細資訊，請參閱 *ole 程式設計人員參考*。</span><span class="sxs-lookup"><span data-stu-id="ba6b5-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




