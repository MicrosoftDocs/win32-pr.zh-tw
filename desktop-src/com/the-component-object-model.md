---
title: 元件物件模型
description: 元件物件模型
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671559"
---
# <a name="the-component-object-model"></a><span data-ttu-id="179c8-103">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="179c8-103">The Component Object Model</span></span>

<span data-ttu-id="179c8-104">Microsoft 元件物件模型 (COM) 是一種與平臺無關、分散式、物件導向的系統，可用來建立可互動的二進位軟體元件。</span><span class="sxs-lookup"><span data-stu-id="179c8-104">The Microsoft Component Object Model (COM) is a platform-independent, distributed, object-oriented system for creating binary software components that can interact.</span></span> <span data-ttu-id="179c8-105">COM 是 Microsoft 的 OLE (複合檔案) 、ActiveX (已啟用網際網路的元件) 和其他專案的基礎技術。</span><span class="sxs-lookup"><span data-stu-id="179c8-105">COM is the foundation technology for Microsoft's OLE (compound documents), ActiveX (Internet-enabled components), as well as others.</span></span>

<span data-ttu-id="179c8-106">若要瞭解 COM (以及所有以 COM 為基礎的技術) ，請務必瞭解這不是物件導向的語言，而是標準的。</span><span class="sxs-lookup"><span data-stu-id="179c8-106">To understand COM (and therefore all COM-based technologies), it is crucial to understand that it is not an object-oriented language but a standard.</span></span> <span data-ttu-id="179c8-107">COM 也不會指定應用程式的結構。語言、結構和執行的詳細資料會留給應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="179c8-107">Nor does COM specify how an application should be structured; language, structure, and implementation details are left to the application developer.</span></span> <span data-ttu-id="179c8-108">相反地，COM 會指定一個物件模型和程式設計需求，讓 COM 物件 (也稱為 COM 元件，或有時候只是) 與其他物件互動的 *物件* 。</span><span class="sxs-lookup"><span data-stu-id="179c8-108">Rather, COM specifies an object model and programming requirements that enable COM objects (also called COM components, or sometimes simply *objects*) to interact with other objects.</span></span> <span data-ttu-id="179c8-109">這些物件可以在單一進程內、在其他進程中，甚至可以在遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="179c8-109">These objects can be within a single process, in other processes, and can even be on remote computers.</span></span> <span data-ttu-id="179c8-110">您可以使用不同的語言來撰寫這些語言，而且它們的結構可能相當不同，這就是為什麼 COM 稱為 *二進位標準*;在程式轉換為二進位機器碼之後套用的標準。</span><span class="sxs-lookup"><span data-stu-id="179c8-110">They can be written in different languages, and they may be structurally quite dissimilar, which is why COM is referred to as a *binary standard*; a standard that applies after a program has been translated to binary machine code.</span></span>

<span data-ttu-id="179c8-111">COM 的唯一語言需求是以可以建立指標結構的語言來產生程式碼，而且可以明確或隱含地透過指標呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="179c8-111">The only language requirement for COM is that code is generated in a language that can create structures of pointers and, either explicitly or implicitly, call functions through pointers.</span></span> <span data-ttu-id="179c8-112">以物件為導向的語言（例如 c + + 和 Smalltalk）提供的程式設計機制可簡化 COM 物件的執行，但 C、JAVA 和 VBScript 等語言可以用來建立和使用 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="179c8-112">Object-oriented languages such as C++ and Smalltalk provide programming mechanisms that simplify the implementation of COM objects, but languages such as C, Java, and VBScript can be used to create and use COM objects.</span></span>

<span data-ttu-id="179c8-113">COM 會定義 COM 物件的基本性質。</span><span class="sxs-lookup"><span data-stu-id="179c8-113">COM defines the essential nature of a COM object.</span></span> <span data-ttu-id="179c8-114">一般情況下，軟體物件是由一組資料和運算元據的函式所組成。</span><span class="sxs-lookup"><span data-stu-id="179c8-114">In general, a software object is made up of a set of data and the functions that manipulate the data.</span></span> <span data-ttu-id="179c8-115">COM 物件是指透過一或多組相關的函式，以獨佔方式來存取物件資料的物件。</span><span class="sxs-lookup"><span data-stu-id="179c8-115">A COM object is one in which access to an object's data is achieved exclusively through one or more sets of related functions.</span></span> <span data-ttu-id="179c8-116">這些函式集合稱為 *介面*，介面的函式稱為 *方法*。</span><span class="sxs-lookup"><span data-stu-id="179c8-116">These function sets are called *interfaces*, and the functions of an interface are called *methods*.</span></span> <span data-ttu-id="179c8-117">此外，COM 要求取得介面方法之存取權的唯一方法是透過介面指標。</span><span class="sxs-lookup"><span data-stu-id="179c8-117">Further, COM requires that the only way to gain access to the methods of an interface is through a pointer to the interface.</span></span>

<span data-ttu-id="179c8-118">除了指定基本的二進位物件標準之外，COM 也會定義特定的基本介面，以提供所有以 COM 為基礎的技術通用的函式，並提供少量的函式，讓所有元件都需要這些功能。</span><span class="sxs-lookup"><span data-stu-id="179c8-118">Besides specifying the basic binary object standard, COM defines certain basic interfaces that provide functions common to all COM-based technologies, and it provides a small number of functions that all components require.</span></span> <span data-ttu-id="179c8-119">COM 也會定義物件如何透過分散式環境一起運作，並已新增安全性功能來協助提供系統和元件的完整性。</span><span class="sxs-lookup"><span data-stu-id="179c8-119">COM also defines how objects work together over a distributed environment and has added security features to help provide system and component integrity.</span></span>

<span data-ttu-id="179c8-120">本節中的下列主題描述與設計 COM 物件相關的基本 COM 問題：</span><span class="sxs-lookup"><span data-stu-id="179c8-120">The following topics in this section describe basic COM issues related to designing COM objects:</span></span>

-   [<span data-ttu-id="179c8-121">COM 物件和介面</span><span class="sxs-lookup"><span data-stu-id="179c8-121">COM Objects and Interfaces</span></span>](com-objects-and-interfaces.md)
-   [<span data-ttu-id="179c8-122">使用和執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="179c8-122">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
-   [<span data-ttu-id="179c8-123">重複使用物件</span><span class="sxs-lookup"><span data-stu-id="179c8-123">Reusing Objects</span></span>](reusing-objects.md)
-   [<span data-ttu-id="179c8-124">COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="179c8-124">The COM Library</span></span>](the-com-library.md)
-   [<span data-ttu-id="179c8-125">管理記憶體配置</span><span class="sxs-lookup"><span data-stu-id="179c8-125">Managing Memory Allocation</span></span>](managing-memory-allocation.md)

 

 




