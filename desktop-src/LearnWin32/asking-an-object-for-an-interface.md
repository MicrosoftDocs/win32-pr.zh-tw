---
title: 要求物件提供介面
description: 要求物件提供介面
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023485"
---
# <a name="asking-an-object-for-an-interface"></a><span data-ttu-id="d92fa-103">要求物件提供介面</span><span class="sxs-lookup"><span data-stu-id="d92fa-103">Asking an Object for an Interface</span></span>

<span data-ttu-id="d92fa-104">我們稍早看到某個物件可以執行多個介面。</span><span class="sxs-lookup"><span data-stu-id="d92fa-104">We saw earlier that an object can implement more than one interface.</span></span> <span data-ttu-id="d92fa-105">一般專案對話方塊物件是這個的真實世界範例。</span><span class="sxs-lookup"><span data-stu-id="d92fa-105">The Common Item Dialog object is a real-world example of this.</span></span> <span data-ttu-id="d92fa-106">為了支援最常見的用法，此物件會實 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面。</span><span class="sxs-lookup"><span data-stu-id="d92fa-106">To support the most typical uses, the object implements the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="d92fa-107">此介面會定義用來顯示對話方塊以及取得所選檔案相關資訊的基本方法。</span><span class="sxs-lookup"><span data-stu-id="d92fa-107">This interface defines basic methods for displaying the dialog box and getting information about the selected file.</span></span> <span data-ttu-id="d92fa-108">不過，若要使用更先進的用法，此物件也會實作為一個名為 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)的介面。</span><span class="sxs-lookup"><span data-stu-id="d92fa-108">For more advanced use, however, the object also implements an interface named [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize).</span></span> <span data-ttu-id="d92fa-109">程式可以使用此介面，藉由加入新的 UI 控制項來自訂對話方塊的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="d92fa-109">A program can use this interface to customize the appearance and behavior of the dialog box, by adding new UI controls.</span></span>

<span data-ttu-id="d92fa-110">回想一下，每個 COM 介面都必須直接或間接繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="d92fa-110">Recall that every COM interface must inherit, directly or indirectly, from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d92fa-111">下圖顯示 [一般專案] 對話方塊物件的繼承。</span><span class="sxs-lookup"><span data-stu-id="d92fa-111">The following diagram shows the inheritance of the Common Item Dialog object.</span></span>

![顯示通用專案對話方塊物件所公開介面的圖表](images/com06.png)

<span data-ttu-id="d92fa-113">您可以從圖表中看到， [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 的直接上階是 [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 介面，接著會繼承 [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)。</span><span class="sxs-lookup"><span data-stu-id="d92fa-113">As you can see from the diagram, the direct ancestor of [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) is the [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface, which in turn inherits [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="d92fa-114">當您將繼承鏈從 **IFileOpenDialog** 移至 **IModalWindow** 時，介面會定義逐漸一般化的視窗功能。</span><span class="sxs-lookup"><span data-stu-id="d92fa-114">As you go up the inheritance chain from **IFileOpenDialog** to **IModalWindow**, the interfaces define increasingly generalized window functionality.</span></span> <span data-ttu-id="d92fa-115">最後， **IModalWindow** 介面會繼承 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)。</span><span class="sxs-lookup"><span data-stu-id="d92fa-115">Finally, the **IModalWindow** interface inherits [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="d92fa-116">一般專案對話方塊物件也會執行存在於不同繼承鏈中的 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)。</span><span class="sxs-lookup"><span data-stu-id="d92fa-116">The Common Item Dialog object also implements [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), which exists in a separate inheritance chain.</span></span>

<span data-ttu-id="d92fa-117">現在假設您有一個指向 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d92fa-117">Now suppose that you have a pointer to the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="d92fa-118">您要如何取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 介面的指標？</span><span class="sxs-lookup"><span data-stu-id="d92fa-118">How would you get a pointer to the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface?</span></span>

![顯示兩個介面指標指向相同物件之介面的圖表](images/com07.png)

<span data-ttu-id="d92fa-120">只要將 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 指標轉換成 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 指標就無法運作。</span><span class="sxs-lookup"><span data-stu-id="d92fa-120">Simply casting the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer to an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer will not work.</span></span> <span data-ttu-id="d92fa-121">沒有可靠的方法可跨繼承階層進行「交叉轉型」，而不會有某種形式的執行時間類型資訊 (RTTI) ，也就是與語言相依的高度特性。</span><span class="sxs-lookup"><span data-stu-id="d92fa-121">There is no reliable way to "cross cast" across an inheritance hierarchy, without some form of run-time type information (RTTI), which is a highly language-dependent feature.</span></span>

<span data-ttu-id="d92fa-122">COM 方法是 *要求* 物件提供您 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 的指標，並使用第一個介面做為物件的管道。</span><span class="sxs-lookup"><span data-stu-id="d92fa-122">The COM approach is to *ask* the object to give you an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer, using the first interface as a conduit into the object.</span></span> <span data-ttu-id="d92fa-123">這是藉由從第一個介面指標呼叫 [**IUnknown：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="d92fa-123">This is done by calling the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method from the first interface pointer.</span></span> <span data-ttu-id="d92fa-124">在 c + + 中，您可以將 **QueryInterface** 視為 **動態 \_ 轉換** 關鍵字的語言獨立版本。</span><span class="sxs-lookup"><span data-stu-id="d92fa-124">You can think of **QueryInterface** as a language-independent version of the **dynamic\_cast** keyword in C++.</span></span>

<span data-ttu-id="d92fa-125">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法具有下列簽章：</span><span class="sxs-lookup"><span data-stu-id="d92fa-125">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method has the following signature:</span></span>

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

<span data-ttu-id="d92fa-126">根據您對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的熟悉程度，您或許可以猜測 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="d92fa-126">Based on what you already know about [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), you might be able to guess how [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) works.</span></span>

-   <span data-ttu-id="d92fa-127">*Riid* 參數是識別您所要求之介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d92fa-127">The *riid* parameter is the GUID that identifies the interface you are asking for.</span></span> <span data-ttu-id="d92fa-128">資料類型 **REFIID** 是的 **typedef** `const GUID&` 。</span><span class="sxs-lookup"><span data-stu-id="d92fa-128">The data type **REFIID** is a **typedef** for `const GUID&`.</span></span> <span data-ttu-id="d92fa-129">請注意，因為物件已經建立，所以不需要 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="d92fa-129">Notice that the class identifier (CLSID) is not required, because the object has already been created.</span></span> <span data-ttu-id="d92fa-130">只有介面識別碼是必要的。</span><span class="sxs-lookup"><span data-stu-id="d92fa-130">Only the interface identifier is necessary.</span></span>
-   <span data-ttu-id="d92fa-131">*PpvObject* 參數會接收介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d92fa-131">The *ppvObject* parameter receives a pointer to the interface.</span></span> <span data-ttu-id="d92fa-132">此參數的資料類型為 **\* \* void**，原因是 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)會使用此資料類型： [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))可用來查詢任何 COM 介面，因此參數不能是強型別。</span><span class="sxs-lookup"><span data-stu-id="d92fa-132">The data type of this parameter is **void\*\***, for the same reason that [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses this data type: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) can be used to query for any COM interface, so the parameter cannot be strongly typed.</span></span>

<span data-ttu-id="d92fa-133">以下是呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 指標的方法：</span><span class="sxs-lookup"><span data-stu-id="d92fa-133">Here is how you would call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer:</span></span>


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="d92fa-134">如往常一樣，請檢查 **HRESULT** 傳回值（如果方法失敗）。</span><span class="sxs-lookup"><span data-stu-id="d92fa-134">As always, check the **HRESULT** return value, in case the method fails.</span></span> <span data-ttu-id="d92fa-135">如果方法成功，您就必須在使用指標完成時呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) ，如 [管理物件的存留期](managing-the-lifetime-of-an-object.md)所述。</span><span class="sxs-lookup"><span data-stu-id="d92fa-135">If the method succeeds, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when you are done using the pointer, as described in [Managing the Lifetime of an Object](managing-the-lifetime-of-an-object.md).</span></span>

## <a name="next"></a><span data-ttu-id="d92fa-136">下一個</span><span class="sxs-lookup"><span data-stu-id="d92fa-136">Next</span></span>

[<span data-ttu-id="d92fa-137">COM 中的記憶體配置</span><span class="sxs-lookup"><span data-stu-id="d92fa-137">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)

 

 