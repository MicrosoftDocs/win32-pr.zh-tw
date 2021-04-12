---
title: 使用直接注釋
description: 使用直接注釋
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315661"
---
# <a name="using-direct-annotation"></a><span data-ttu-id="ec1a9-103">使用直接注釋</span><span class="sxs-lookup"><span data-stu-id="ec1a9-103">Using Direct Annotation</span></span>

<span data-ttu-id="ec1a9-104">**若要使用直接注釋來覆寫屬性的值**</span><span class="sxs-lookup"><span data-stu-id="ec1a9-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="ec1a9-105">使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) 函式來建立 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 物件。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="ec1a9-106">呼叫 [**IAccPropServices：： SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop)，傳遞 **HWND**、物件識別碼、子識別碼、要覆寫的屬性，以及包含屬性新值的 [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) 。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="ec1a9-107">此步驟會標注值。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="ec1a9-108">釋放介面指標和可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="ec1a9-109">下列範例顯示如何標注靜態文字控制項的 [**Role**](role-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="ec1a9-110">指定值時支援的屬性</span><span class="sxs-lookup"><span data-stu-id="ec1a9-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="ec1a9-111">當您指定值時，可以標注下列 Microsoft Active Accessibility 屬性 (其中的值必須是直接注釋) 的附注型別。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="ec1a9-112">若要覆寫或加入 Microsoft 消費者介面自動化屬性至控制項，您可以指定消費者介面自動化屬性識別碼，而不是 Microsoft Active Accessibility 屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="ec1a9-113">如需消費者介面自動化識別碼的清單，請參閱 [屬性識別碼](uiauto-entry-propids.md)。</span><span class="sxs-lookup"><span data-stu-id="ec1a9-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="ec1a9-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ec1a9-114">Property</span></span>                      | <span data-ttu-id="ec1a9-115">類型</span><span class="sxs-lookup"><span data-stu-id="ec1a9-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="ec1a9-116">PROPID \_ ACC \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="ec1a9-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="ec1a9-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-117">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-118">PROPID \_ ACC \_ 描述</span><span class="sxs-lookup"><span data-stu-id="ec1a9-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="ec1a9-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-119">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-120">PROPID \_ ACC \_ 角色</span><span class="sxs-lookup"><span data-stu-id="ec1a9-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="ec1a9-121">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ec1a9-121">VT\_I4</span></span>   |
| <span data-ttu-id="ec1a9-122">PROPID \_ ACC \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="ec1a9-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="ec1a9-123">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ec1a9-123">VT\_I4</span></span>   |
| <span data-ttu-id="ec1a9-124">PROPID \_ ACC \_ 說明</span><span class="sxs-lookup"><span data-stu-id="ec1a9-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="ec1a9-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-125">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-126">PROPID \_ ACC \_ KEYBOARDSHORTCUT</span><span class="sxs-lookup"><span data-stu-id="ec1a9-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="ec1a9-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-127">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-128">PROPID \_ ACC \_ DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="ec1a9-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="ec1a9-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-129">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-130">PROPID \_ ACC 的 \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="ec1a9-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="ec1a9-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-131">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-132">PROPID \_ ACC \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="ec1a9-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="ec1a9-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-133">VT\_BSTR</span></span> |
| <span data-ttu-id="ec1a9-134">PROPID \_ ACC \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="ec1a9-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="ec1a9-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ec1a9-135">VT\_BSTR</span></span> |



 

 

 