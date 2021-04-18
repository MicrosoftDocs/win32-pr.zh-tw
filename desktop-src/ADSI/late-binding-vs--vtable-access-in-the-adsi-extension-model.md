---
title: ADSI 擴充模型中的晚期繫結與 Vtable 存取
description: 雙重介面可讓您在分派介面沒有時，對其所有的函式進行直接 vtable 存取。
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- ADSI 擴充模型 ADSI 中的晚期繫結與 vtable 存取
- ADSI 擴充模型中的延伸 ADSI、晚期繫結和 vtable 存取
- ADSI ADSI，範例程式碼 Visual Basic，使用 IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106983304"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="30b9e-106">ADSI 擴充模型中的晚期繫結與 Vtable 存取</span><span class="sxs-lookup"><span data-stu-id="30b9e-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="30b9e-107">雙重介面可讓您在分派介面沒有時，對其所有的函式進行直接 vtable 存取。</span><span class="sxs-lookup"><span data-stu-id="30b9e-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="30b9e-108">C/c + + 用戶端可以查詢雙重介面指標，並使用直接 vtable 存取來叫用其函數。</span><span class="sxs-lookup"><span data-stu-id="30b9e-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="30b9e-109">這可提供比使用 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**Idispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 函數叫用函式更快的存取權。</span><span class="sxs-lookup"><span data-stu-id="30b9e-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="30b9e-110">這在擴充模型中更是如此，因為擴充功能物件中的所有雙重介面都必須先委派其 **GetIDsOfNames** **，並** 將函式重新叫用至匯總工具 (ADSI) first。</span><span class="sxs-lookup"><span data-stu-id="30b9e-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="30b9e-111">然後，匯總工具必須執行額外的內部步驟，以識別哪個擴充物件（可能包含匯總工具本身）支援呼叫的函式，並將呼叫重新導向至適當的物件。</span><span class="sxs-lookup"><span data-stu-id="30b9e-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="30b9e-112">Visual Basic 也會使用 vtable 的直接存取叫用雙重介面函式（如果它有介面的指標，並從類型程式庫存取型別資料）。</span><span class="sxs-lookup"><span data-stu-id="30b9e-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="30b9e-113">以 Visual Basic 撰寫的 ADSI 用戶端可以指定雙重介面的指標，例如 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、明確地，並允許 vtable 存取介面中的函式。</span><span class="sxs-lookup"><span data-stu-id="30b9e-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="30b9e-114">由於 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面不支援 vtable 存取，因此不適用此範例。</span><span class="sxs-lookup"><span data-stu-id="30b9e-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="30b9e-115">也就是說，只會透過 [**idispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**Idispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 函數叫用分派函式。</span><span class="sxs-lookup"><span data-stu-id="30b9e-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="30b9e-116">目前的 VBScript 和 JScript 版本也不支援 vtable 存取。</span><span class="sxs-lookup"><span data-stu-id="30b9e-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="30b9e-117">因此，VBScript 或 JScript 環境中的雙重介面會像分派介面一樣執行。</span><span class="sxs-lookup"><span data-stu-id="30b9e-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 