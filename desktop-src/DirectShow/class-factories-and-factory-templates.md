---
description: 本主題說明如何使用 DirectShow 基類，為 DirectShow 篩選器執行 DLL。
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Class factory 和 Factory 範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567180"
---
# <a name="class-factories-and-factory-templates"></a><span data-ttu-id="53692-103">Class factory 和 Factory 範本</span><span class="sxs-lookup"><span data-stu-id="53692-103">Class Factories and Factory Templates</span></span>

<span data-ttu-id="53692-104">本主題說明如何使用 [Directshow 基類](directshow-base-classes.md)，為 directshow 篩選器執行 DLL。</span><span class="sxs-lookup"><span data-stu-id="53692-104">This topic describes how to implement a DLL for a DirectShow filter, using the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

<span data-ttu-id="53692-105">在用戶端建立 COM 物件的實例之前，它會使用 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 函數的呼叫，建立物件的 class factory 實例。</span><span class="sxs-lookup"><span data-stu-id="53692-105">Before a client creates an instance of a COM object, it creates an instance of the object's class factory, using a call to the [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) function.</span></span> <span data-ttu-id="53692-106">然後，用戶端會呼叫 class factory 的 **IClassFactory：： CreateInstance** 方法。</span><span class="sxs-lookup"><span data-stu-id="53692-106">The client then calls the class factory's **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="53692-107">它是實際建立元件並傳回所要求介面之指標的 class factory。</span><span class="sxs-lookup"><span data-stu-id="53692-107">It is the class factory that actually creates the component and returns a pointer to the requested interface.</span></span> <span data-ttu-id="53692-108"> ([**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會在函式呼叫內合併這些步驟。 ) </span><span class="sxs-lookup"><span data-stu-id="53692-108">(The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function combines these steps, inside the function call.)</span></span>

<span data-ttu-id="53692-109">下圖顯示方法呼叫的順序。</span><span class="sxs-lookup"><span data-stu-id="53692-109">The following illustration shows the sequence of method calls.</span></span>

![建立 class factory 的方法呼叫](images/classfactory.png)

<span data-ttu-id="53692-111">[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 會呼叫 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式，該函式是在 DLL 中定義。</span><span class="sxs-lookup"><span data-stu-id="53692-111">[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) calls the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function, which is defined in the DLL.</span></span> <span data-ttu-id="53692-112">此函式會建立 class factory，並將指標傳回給 class factory 上的介面。</span><span class="sxs-lookup"><span data-stu-id="53692-112">This function creates the class factory and returns a pointer to an interface on the class factory.</span></span> <span data-ttu-id="53692-113">DirectShow 為您實 **DllGetClassObject** ，但函式依賴您的程式碼以特定方式運作。</span><span class="sxs-lookup"><span data-stu-id="53692-113">DirectShow implements **DllGetClassObject** for you, but the function relies on your code in a specific way.</span></span> <span data-ttu-id="53692-114">若要瞭解其運作方式，您必須瞭解 DirectShow 如何實行 class factory。</span><span class="sxs-lookup"><span data-stu-id="53692-114">To understand how it works, you must understand how DirectShow implements class factories.</span></span>

<span data-ttu-id="53692-115">Class factory 是專門用來建立另一個 COM 物件的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="53692-115">A class factory is a COM object dedicated to creating another COM object.</span></span> <span data-ttu-id="53692-116">每個 class factory 都有一個它所建立的物件類型。</span><span class="sxs-lookup"><span data-stu-id="53692-116">Each class factory has one type of object that it creates.</span></span> <span data-ttu-id="53692-117">在 DirectShow 中，每個 class factory 都是相同 c + + 類別 **CClassFactory** 的實例。</span><span class="sxs-lookup"><span data-stu-id="53692-117">In DirectShow, every class factory is an instance of the same C++ class, **CClassFactory**.</span></span> <span data-ttu-id="53692-118">Class factory 是透過另一個類別 [**CFactoryTemplate**](cfactorytemplate.md)來特製化，也稱為 *factory 範本*。</span><span class="sxs-lookup"><span data-stu-id="53692-118">Class factories are specialized by means of another class, [**CFactoryTemplate**](cfactorytemplate.md), also called the *factory template*.</span></span> <span data-ttu-id="53692-119">每個 class factory 都會保留一個指向 factory 範本的指標。</span><span class="sxs-lookup"><span data-stu-id="53692-119">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="53692-120">Factory 範本包含特定元件的相關資訊，例如元件的類別識別碼 (CLSID) ，以及函式的指標，該函式會建立元件。</span><span class="sxs-lookup"><span data-stu-id="53692-120">The factory template contains information about a specific component, such as the component's class identifier (CLSID), and a pointer to a function that creates the component.</span></span>

<span data-ttu-id="53692-121">DLL 會宣告原廠範本的全域陣列，DLL 中的每個元件都有一個。</span><span class="sxs-lookup"><span data-stu-id="53692-121">The DLL declares a global array of factory templates, one for each component in the DLL.</span></span> <span data-ttu-id="53692-122">當 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 建立新的 class factory 時，它會在陣列中搜尋具有相符 CLSID 的範本。</span><span class="sxs-lookup"><span data-stu-id="53692-122">When [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="53692-123">假設找到一個，它會建立一個持有相符範本指標的 class factory。</span><span class="sxs-lookup"><span data-stu-id="53692-123">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="53692-124">當用戶端呼叫 **IClassFactory：： CreateInstance** 時，class factory 會呼叫範本中定義的具現化函數。</span><span class="sxs-lookup"><span data-stu-id="53692-124">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="53692-125">下圖顯示方法呼叫的順序。</span><span class="sxs-lookup"><span data-stu-id="53692-125">The following illustration shows the sequence of method calls.</span></span>

![dll 中的 class factory 範本](images/classfactory2.png)

<span data-ttu-id="53692-127">此架構的優點是，您只能定義您的元件專屬的一些專案，例如具現化函數，而不需要執行整個 class factory。</span><span class="sxs-lookup"><span data-stu-id="53692-127">The benefit of this architecture is that you can define just a few things that are specific to your component, such as the instantiation function, without implementing the entire class factory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53692-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="53692-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53692-129">如何建立 DirectShow 篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="53692-129">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
