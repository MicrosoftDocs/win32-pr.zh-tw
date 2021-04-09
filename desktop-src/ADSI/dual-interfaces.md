---
title: " (ADSI) 的雙重介面"
description: 使用 COM 介面存取任何提供者 ADSI 物件上的屬性和方法。
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683079"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="58736-103"> (ADSI) 的雙重介面</span><span class="sxs-lookup"><span data-stu-id="58736-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="58736-104">使用 COM 介面存取任何提供者 ADSI 物件上的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="58736-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="58736-105">唯讀屬性會對應至表單 **get \_ <PropertyName>** 的介面專案。</span><span class="sxs-lookup"><span data-stu-id="58736-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="58736-106">讀取/寫入屬性會對應到 **get \_ <PropertyName>** 和 **put \_ <PropertyName>** 格式的兩個介面專案。</span><span class="sxs-lookup"><span data-stu-id="58736-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="58736-107">COM 介面上的所有方法都必須：</span><span class="sxs-lookup"><span data-stu-id="58736-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="58736-108">傳回 HRESULT 值以表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="58736-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="58736-109">**HRESULT** 型別會在 COM 規格中討論。</span><span class="sxs-lookup"><span data-stu-id="58736-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="58736-110">在對 **QueryInterface** 的呼叫中，傳回未實現介面的 **E \_ NOINTERFACE** 。</span><span class="sxs-lookup"><span data-stu-id="58736-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="58736-111">針對未在其他方式執行的介面傳回未完成之方法的 **E \_ >notimpl** 。</span><span class="sxs-lookup"><span data-stu-id="58736-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="58736-112">不支援的介面屬性 **\_ \_ \_ 不 \_ 支援傳回 E ADS 屬性** 。</span><span class="sxs-lookup"><span data-stu-id="58736-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="58736-113">為了維持與 Automation 控制器的相容性，所有參數和傳回類型都應該在 Automation VARIANT 資料類型所定義的子集內。</span><span class="sxs-lookup"><span data-stu-id="58736-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="58736-114">如需詳細資訊，請參閱平臺軟體發展工具組中的 **變異** 和 **VARIANTARG** (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="58736-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="58736-115">提供者 Active Directory 物件可以公開使用 **變數** 子集中以外之資料類型的介面。</span><span class="sxs-lookup"><span data-stu-id="58736-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="58736-116">不過，Visual Basic 的 Automation 控制器無法呼叫這些介面。</span><span class="sxs-lookup"><span data-stu-id="58736-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="58736-117">大部分的 ADSI 提供者介面都是衍生自 [**idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ，而且可以當做 **idispatch** 介面指標使用。</span><span class="sxs-lookup"><span data-stu-id="58736-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="58736-118">但是， [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)、 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)和 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI 介面不是衍生自 **IDispatch**。</span><span class="sxs-lookup"><span data-stu-id="58736-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 