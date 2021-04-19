---
description: 檢查產生器是否應該與特定屬性相關聯。
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: IProvidePropertyBuilder：： MapPropertyToBuilder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995619"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="5adaf-103">IProvidePropertyBuilder：： MapPropertyToBuilder 方法</span><span class="sxs-lookup"><span data-stu-id="5adaf-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="5adaf-104">檢查產生器是否應該與特定屬性相關聯。</span><span class="sxs-lookup"><span data-stu-id="5adaf-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5adaf-105">語法</span><span class="sxs-lookup"><span data-stu-id="5adaf-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="5adaf-106">參數</span><span class="sxs-lookup"><span data-stu-id="5adaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5adaf-107">*dispid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5adaf-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5adaf-108">有問題的屬性 DISPID。</span><span class="sxs-lookup"><span data-stu-id="5adaf-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="5adaf-109">*pdwCtlBldType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5adaf-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5adaf-110">要對應的 builder。</span><span class="sxs-lookup"><span data-stu-id="5adaf-110">The builder to be mapped.</span></span> <span data-ttu-id="5adaf-111">這個參數可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="5adaf-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="5adaf-112">值</span><span class="sxs-lookup"><span data-stu-id="5adaf-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="5adaf-113">意義</span><span class="sxs-lookup"><span data-stu-id="5adaf-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="5adaf-114"><dt>**CTLBLDTYPE \_FSTDPROPBUILDER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5adaf-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="5adaf-115">在 Visual Studio) 中不支援叫用標準系統產生器 (。</span><span class="sxs-lookup"><span data-stu-id="5adaf-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="5adaf-116"><dt>**CTLBLDTYPE \_FINTERNALBUILDER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5adaf-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5adaf-117">叫用自訂產生器。</span><span class="sxs-lookup"><span data-stu-id="5adaf-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="5adaf-118"><dt>**CTLBLDTYPE \_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5adaf-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="5adaf-119">Builder 會修改物件。</span><span class="sxs-lookup"><span data-stu-id="5adaf-119">Builder modifies the object.</span></span> <span data-ttu-id="5adaf-120">這是常見的行為。</span><span class="sxs-lookup"><span data-stu-id="5adaf-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="5adaf-121">*pbstrGuidBldr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5adaf-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5adaf-122">識別此屬性之產生器的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5adaf-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="5adaf-123">*builderAvailable* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5adaf-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5adaf-124">如果這個屬性目前支援產生器，此參數為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5adaf-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5adaf-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="5adaf-125">Return value</span></span>

<span data-ttu-id="5adaf-126">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5adaf-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5adaf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5adaf-127">Requirements</span></span>



| <span data-ttu-id="5adaf-128">需求</span><span class="sxs-lookup"><span data-stu-id="5adaf-128">Requirement</span></span> | <span data-ttu-id="5adaf-129">值</span><span class="sxs-lookup"><span data-stu-id="5adaf-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5adaf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5adaf-130">DLL</span></span><br/> | <dl> <span data-ttu-id="5adaf-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5adaf-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5adaf-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5adaf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5adaf-133">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="5adaf-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




