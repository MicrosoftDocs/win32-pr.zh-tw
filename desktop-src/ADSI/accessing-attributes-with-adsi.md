---
title: 使用 ADSI 存取屬性
description: IADs 和 IADs. GetEx 方法是用來取出指名的屬性值。
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 存取的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966887"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="6fc99-104">使用 ADSI 存取屬性</span><span class="sxs-lookup"><span data-stu-id="6fc99-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="6fc99-105">[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法是用來取出指名的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6fc99-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="6fc99-106">這兩種方法都會傳回 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant) 值。</span><span class="sxs-lookup"><span data-stu-id="6fc99-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="6fc99-107">這些方法僅適用于支援架構的目錄。</span><span class="sxs-lookup"><span data-stu-id="6fc99-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="6fc99-108">存取沒有架構的目錄中的物件時，必須使用 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) 和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 介面來操作屬性值。</span><span class="sxs-lookup"><span data-stu-id="6fc99-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="6fc99-109">[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-getex)會根據伺服器傳回的值數目，傳回可能（或可能不是）**變數** 陣列的 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant)。</span><span class="sxs-lookup"><span data-stu-id="6fc99-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="6fc99-110">例如，如果伺服器只傳回一個值，而不論它是單一值或多重值屬性，則方法會傳回單一 **VARIANT**。</span><span class="sxs-lookup"><span data-stu-id="6fc99-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="6fc99-111">相反地，如果傳回多個值，則會傳回 **VARIANT** 陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc99-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="6fc99-112">如果傳回 **variant** 陣列， **variant** 結構的 **vt** 成員會包含 **vt \_ VARIANT/vbVariant** 和 **vt \_ array/vbArray** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6fc99-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="6fc99-113">[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)和 [**IADs 的 GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)方法也可以使用 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面傳回 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="6fc99-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6fc99-114">在此情況下， [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員會包含 **vt \_ 分派/vbObject** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6fc99-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="6fc99-115">若要存取 COM 物件，請呼叫 **IDispatch** 介面上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得所需的介面。</span><span class="sxs-lookup"><span data-stu-id="6fc99-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="6fc99-116">[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get)所傳回的另一個資料類型為二進位 [**資料。**](/windows/desktop/api/Iads/nf-iads-iads-getex)</span><span class="sxs-lookup"><span data-stu-id="6fc99-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="6fc99-117">在此情況下，資料會以連續的位元組陣列形式提供，而 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員將包含 **Vt \_ UI1/vbByte** 和 **vt \_ array/vbArray** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6fc99-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="6fc99-118">Microsoft Visual Basic，腳本撰寫版僅支援 [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant) 和 **variant** 陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc99-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="6fc99-119">因此，VBScript 無法用來讀取二進位屬性值。</span><span class="sxs-lookup"><span data-stu-id="6fc99-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="6fc99-120">許多 ADSI 介面會定義介面特定屬性。</span><span class="sxs-lookup"><span data-stu-id="6fc99-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="6fc99-121">例如， [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) 介面會定義 [**Location**](iadscomputer-property-methods.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6fc99-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="6fc99-122">這些介面定義的屬性可能包含與其中一個已命名屬性相同的資料，但這些屬性是由介面所參考的物件類型所特有。</span><span class="sxs-lookup"><span data-stu-id="6fc99-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="6fc99-123">在支援自動化的語言中，您可以使用點標記法來存取這些介面定義的屬性，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="6fc99-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="6fc99-124">範例</span><span class="sxs-lookup"><span data-stu-id="6fc99-124">Examples</span></span>

<span data-ttu-id="6fc99-125">下列程式碼範例顯示如何存取 IADs 介面上的 ADsPath 屬性。</span><span class="sxs-lookup"><span data-stu-id="6fc99-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="6fc99-126">在非自動化語言中，必須使用屬性存取方法來存取介面定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="6fc99-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="6fc99-127">例如， [**IADsComputer：： get \_ Location**](iadscomputer-property-methods.md) 方法是用來取出 **IADsComputer. location** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6fc99-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="6fc99-128">下列 c + + 程式碼範例示範如何在 c + + 中使用屬性存取方法，以取得使用者的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="6fc99-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="6fc99-129">如需使用 ADSI 存取屬性的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="6fc99-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="6fc99-130">Get 方法</span><span class="sxs-lookup"><span data-stu-id="6fc99-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="6fc99-131">GetEx 方法</span><span class="sxs-lookup"><span data-stu-id="6fc99-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="6fc99-132">GetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6fc99-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="6fc99-133">使用 GetInfoEx 的優化</span><span class="sxs-lookup"><span data-stu-id="6fc99-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="6fc99-134">使用 IDirectoryObject 介面存取屬性</span><span class="sxs-lookup"><span data-stu-id="6fc99-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="6fc99-135">用於讀取屬性的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6fc99-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 