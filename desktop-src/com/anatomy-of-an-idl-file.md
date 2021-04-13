---
title: IDL 檔案的剖析
description: 這些範例 IDL 檔案示範介面定義的基礎結構。
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "104321380"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="0425f-103">IDL 檔案的剖析</span><span class="sxs-lookup"><span data-stu-id="0425f-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="0425f-104">這些範例 IDL 檔案示範介面定義的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="0425f-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="0425f-105">記憶體配置、自訂封送處理和非同步訊息只是您可以在自訂 COM 介面中執行的幾項功能。</span><span class="sxs-lookup"><span data-stu-id="0425f-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="0425f-106">MIDL 屬性是用來定義 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0425f-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="0425f-107">如需有關如何執行介面和型別程式庫的詳細資訊，包括 MIDL 屬性的摘要，請參閱 MIDL 程式設計師指南和參考中的 [介面定義和型別程式庫](/windows/desktop/Midl/interface-definitions-and-type-libraries) 。</span><span class="sxs-lookup"><span data-stu-id="0425f-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="0425f-108">如需所有 MIDL 屬性、關鍵字和指示詞的完整參考，請參閱 [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)。</span><span class="sxs-lookup"><span data-stu-id="0425f-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="0425f-109">範例 .idl</span><span class="sxs-lookup"><span data-stu-id="0425f-109">Example.idl</span></span>

<span data-ttu-id="0425f-110">下列範例 IDL 檔案會定義兩個 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0425f-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="0425f-111">從這個 IDL 檔案，Midl.exe 將會產生 proxy/stub，以及封送處理常式代碼和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="0425f-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="0425f-112">剖析會遵循範例。</span><span class="sxs-lookup"><span data-stu-id="0425f-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="0425f-113">在這裡使用 IDL 匯 [**入**](/windows/desktop/Midl/import) 語句來帶入標頭檔（Mydefs），其中包含使用者定義型別，以及 Unknwn 包含 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的定義，其中 IFace1 和 IFace2 衍生自後者。</span><span class="sxs-lookup"><span data-stu-id="0425f-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="0425f-114">[**Object**](/windows/desktop/Midl/object)屬性將介面識別為物件介面，並告知 MIDL 編譯器產生 proxy/stub 程式碼，而不是 RPC 用戶端和伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="0425f-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="0425f-115">物件介面方法的傳回類型必須是 [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)，以允許基礎 RPC 機制回報因網路問題而無法完成的呼叫錯誤。</span><span class="sxs-lookup"><span data-stu-id="0425f-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="0425f-116">[**Uuid**](/windows/desktop/Midl/uuid)屬性會指定 (IID) 的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="0425f-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="0425f-117">每個介面、類別和類型程式庫都必須使用自己的唯一識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="0425f-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="0425f-118">使用公用程式 Uuidgen.exe 為您的介面和其他元件產生一組唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0425f-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="0425f-119">[**Interface**](/windows/desktop/Midl/interface)關鍵字會定義介面名稱。</span><span class="sxs-lookup"><span data-stu-id="0425f-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="0425f-120">所有物件介面都必須直接或間接衍生自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)。</span><span class="sxs-lookup"><span data-stu-id="0425f-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="0425f-121">[**In**](/windows/desktop/Midl/in)方向參數指定僅由呼叫端設定的參數。</span><span class="sxs-lookup"><span data-stu-id="0425f-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="0425f-122">[**Out**](/windows/desktop/Midl/out-idl)參數會指定傳回給呼叫端的資料。</span><span class="sxs-lookup"><span data-stu-id="0425f-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="0425f-123">在一個參數上使用這兩個方向屬性，可指定使用參數將資料傳送至方法，並將資料傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="0425f-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="0425f-124">[**指標 \_ default**](/windows/desktop/Midl/pointer-default)屬性指定預設指標類型 (除了參數清單中包含的所有指標以外的 [**唯一**](/windows/desktop/Midl/unique)、 [**ref**](/windows/desktop/Midl/ref)或 [**ptr**](/windows/desktop/Midl/ptr)) 。</span><span class="sxs-lookup"><span data-stu-id="0425f-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="0425f-125">如果未指定預設型別，MIDL 會假設單一指標是 **唯一** 的。</span><span class="sxs-lookup"><span data-stu-id="0425f-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="0425f-126">但是，當您有多個層級的指標時，您必須明確指定預設的指標類型，即使您想要讓預設型別成為 **唯一** 的。</span><span class="sxs-lookup"><span data-stu-id="0425f-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="0425f-127">在上述範例中，陣列 BkfstStuff \[ \] 是 *符合標準的陣列*，這是在執行時間決定的大小。</span><span class="sxs-lookup"><span data-stu-id="0425f-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="0425f-128">[**Max \_ 為**](/windows/desktop/Midl/max-is)attribute 指定包含陣列索引最大值的變數。</span><span class="sxs-lookup"><span data-stu-id="0425f-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="0425f-129">[**Size \_ 為**](/windows/desktop/Midl/size-is)attribute 也用來指定陣列的大小，或（如同上述範例中的多個指標層級）。</span><span class="sxs-lookup"><span data-stu-id="0425f-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="0425f-130">在此範例中，您可以在不事先知道將傳回多少資料的情況下進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="0425f-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="0425f-131">Example2 .idl</span><span class="sxs-lookup"><span data-stu-id="0425f-131">Example2.idl</span></span>

<span data-ttu-id="0425f-132">下列 IDL 範例 (會重複使用先前 IDL 範例中所述的介面) 顯示產生介面類別型庫資訊的各種方法。</span><span class="sxs-lookup"><span data-stu-id="0425f-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="0425f-133">[**Helpstring**](/windows/desktop/Midl/helpstring)屬性是選擇性的;您可以使用它來簡短描述物件或提供狀態行。</span><span class="sxs-lookup"><span data-stu-id="0425f-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="0425f-134">這些說明字串可使用物件瀏覽器來讀取，例如 Microsoft Visual Basic 所提供的物件瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="0425f-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="0425f-135">IFace3 上的 [**雙重**](/windows/desktop/Midl/dual) 屬性會建立同時為分派介面和 COM 介面的介面。</span><span class="sxs-lookup"><span data-stu-id="0425f-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="0425f-136">因為它衍生自 **IDispatch**，所以雙重介面支援 Automation，也就是 [**oleautomation**](/windows/desktop/Midl/oleautomation) 屬性所指定的。</span><span class="sxs-lookup"><span data-stu-id="0425f-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="0425f-137">IFace3 會匯入 Oaidl.idl，以取得 **IDispatch** 的定義。</span><span class="sxs-lookup"><span data-stu-id="0425f-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="0425f-138">[**Library**](/windows/desktop/Midl/library)語句會定義 ExampleLib 類型程式庫，其具有自己的 [**uuid**](/windows/desktop/Midl/uuid)、 [**helpstring**](/windows/desktop/Midl/helpstring)和 [**version**](/windows/desktop/Midl/version)屬性。</span><span class="sxs-lookup"><span data-stu-id="0425f-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="0425f-139">在類型程式庫定義內， [**importlib**](/windows/desktop/Midl/importlib) 指示詞會帶入已編譯的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="0425f-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="0425f-140">所有類型程式庫定義都應該帶入 Stdole32 中定義的基底類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="0425f-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="0425f-141">此類型程式庫定義示範三種不同的方式，可將介面包含在類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="0425f-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="0425f-142">IFace3 只會在程式庫語句內進行參考而包含在內。</span><span class="sxs-lookup"><span data-stu-id="0425f-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="0425f-143">[**Coclass**](/windows/desktop/Midl/coclass)語句會定義全新的元件類別 BkfstComponent，其中包含兩個先前定義的介面 IFace1 和 IFace2。</span><span class="sxs-lookup"><span data-stu-id="0425f-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="0425f-144">預設屬性會將 IFace1 指定為預設介面。</span><span class="sxs-lookup"><span data-stu-id="0425f-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="0425f-145">IFace4 描述于 library 語句內。</span><span class="sxs-lookup"><span data-stu-id="0425f-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="0425f-146">MethodD 上的 [**propput**](/windows/desktop/Midl/propput) 屬性工作表示方法會在相同名稱的屬性上執行設定動作。</span><span class="sxs-lookup"><span data-stu-id="0425f-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="0425f-147">[**Propget**](/windows/desktop/Midl/propget)屬性指出方法會從與方法相同名稱的屬性中抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="0425f-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="0425f-148">MethodD 中的 [**retval**](/windows/desktop/Midl/retval) 屬性指定輸出參數，其中包含函式的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0425f-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
