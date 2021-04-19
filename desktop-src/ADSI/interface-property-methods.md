---
title: 介面屬性方法
description: 許多 ADSI 介面都是設計來支援自動化，因此也是雙重介面，因為它們支援透過 IUnknown 和 IDispatch 介面的用戶端存取。
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- 介面屬性方法
- 說明 ADSI ADSI、參考、屬性方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106967693"
---
# <a name="interface-property-methods"></a><span data-ttu-id="80744-105">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="80744-105">Interface Property Methods</span></span>

<span data-ttu-id="80744-106">許多 ADSI 介面都是設計來支援自動化，因此也是雙重介面，因為它們支援透過 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面的用戶端存取。</span><span class="sxs-lookup"><span data-stu-id="80744-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="80744-107">非自動化用戶端（例如以 C/c + + 撰寫的用戶端）會使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法直接解析方法調用，並直接呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="80744-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="80744-108">Automation 用戶端（也稱為名稱系結用戶端，例如以 Visual Basic 撰寫的用戶端，或 Visual Basic Scripting Edition (VBScript) ）必須使用分派 [**介面**](/previous-versions/windows/desktop/automat/dispinterface) 方法間接解析方法調用。</span><span class="sxs-lookup"><span data-stu-id="80744-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="80744-109">支援 Automation 的 ADSI 介面會定義屬性方法，以抓取和修改執行介面之物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="80744-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="80744-110">屬性方法的名稱會 \_  \_ 在適當的屬性名稱前面加上 get 和 put，例如， **get \_ User** 和 **put \_ Name**。</span><span class="sxs-lookup"><span data-stu-id="80744-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="80744-111">每 **個 \_ get** 方法都採用單一參數作為輸出。</span><span class="sxs-lookup"><span data-stu-id="80744-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="80744-112">這個參數是屬性資料類型之變數的方法配置位址。</span><span class="sxs-lookup"><span data-stu-id="80744-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="80744-113">傳回時，這個變數會假設所要求屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="80744-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="80744-114">當不再需要屬性時，呼叫端必須釋放變數的配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="80744-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="80744-115">每 **個 \_ put** 方法都採用單一參數作為對應屬性之資料類型的輸入。</span><span class="sxs-lookup"><span data-stu-id="80744-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="80744-116">參數會保存新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="80744-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="80744-117">下列程式碼範例顯示內容方法的調用，這些方法會遵循一般程式來呼叫物件的成員函式。</span><span class="sxs-lookup"><span data-stu-id="80744-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="80744-118">下列程式碼範例示範如何在 automation 用戶端中叫用屬性方法，這種方法可能稍有不同。</span><span class="sxs-lookup"><span data-stu-id="80744-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="80744-119">例如，Visual Basic 會使用點標記法。</span><span class="sxs-lookup"><span data-stu-id="80744-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="80744-120">所有參數和傳回類型都必須屬於 VARIANT 資料類型所定義的參數和傳回型別。</span><span class="sxs-lookup"><span data-stu-id="80744-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="80744-121">雙重介面上的所有方法都會傳回 HRESULT 值，以表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="80744-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="80744-122">如需有關在 ADSI 物件上取得和設定屬性的詳細資訊，請參閱 [屬性](property-cache-interfaces.md)快取。</span><span class="sxs-lookup"><span data-stu-id="80744-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 