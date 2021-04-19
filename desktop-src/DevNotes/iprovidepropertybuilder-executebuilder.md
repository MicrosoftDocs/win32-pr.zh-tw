---
description: 通知物件應針對指定的屬性顯示其產生器。
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: IProvidePropertyBuilder：： ExecuteBuilder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975974"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="1f0d0-103">IProvidePropertyBuilder：： ExecuteBuilder 方法</span><span class="sxs-lookup"><span data-stu-id="1f0d0-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="1f0d0-104">通知物件應針對指定的屬性顯示其產生器。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f0d0-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="1f0d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0d0-107">*dispid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-108">產生器所顯示的屬性 DISPID。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="1f0d0-109">*bstrGuidBldr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-110">要叫用之產生器 GUID 的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="1f0d0-111">這會從 [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f0d0-112">*pdispApp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-113">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f0d0-114">*hwndBldrOwner* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-115">父代彈出產生器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="1f0d0-116">*pvarValue* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-117">屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-117">The current value of the property.</span></span> <span data-ttu-id="1f0d0-118">如果 *pbActionCommitted* 為 TRUE，則物件可以修改此值，並將新值變更為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="1f0d0-119">*pbActionCommitted* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="1f0d0-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0d0-120">值，這個值會指出 builder 是否在物件上執行動作。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="1f0d0-121">可以在使用者修改某個內容時使用，然後在快顯產生器對話方塊上按 [確定]。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0d0-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f0d0-122">Return value</span></span>

<span data-ttu-id="1f0d0-123">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1f0d0-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0d0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f0d0-124">Requirements</span></span>



| <span data-ttu-id="1f0d0-125">需求</span><span class="sxs-lookup"><span data-stu-id="1f0d0-125">Requirement</span></span> | <span data-ttu-id="1f0d0-126">值</span><span class="sxs-lookup"><span data-stu-id="1f0d0-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0d0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1f0d0-127">DLL</span></span><br/> | <dl> <span data-ttu-id="1f0d0-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f0d0-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f0d0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f0d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f0d0-130">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="1f0d0-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




