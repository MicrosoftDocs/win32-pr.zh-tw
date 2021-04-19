---
description: 取得在中指定之子屬性的值。 <Properties> 掃描設定檔的元素。
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile：： GetProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974140"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="c1e2c-104">IScanProfile：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="c1e2c-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="c1e2c-105">取得掃描設定檔的元素中指定之子屬性的值 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e2c-106">語法</span><span class="sxs-lookup"><span data-stu-id="c1e2c-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="c1e2c-107">參數</span><span class="sxs-lookup"><span data-stu-id="c1e2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e2c-108">*num* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1e2c-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e2c-109">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="c1e2c-109">Type: **ULONG**</span></span>

<span data-ttu-id="c1e2c-110">由 *pid* 和 *pvar* 指向的陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="c1e2c-111">*pid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1e2c-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e2c-112">類型： \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="c1e2c-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="c1e2c-113">要設定之屬性識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="c1e2c-114">陣列中的每個值都是 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1e2c-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c1e2c-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e2c-116">類型： \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="c1e2c-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="c1e2c-117">值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e2c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1e2c-118">Return value</span></span>

<span data-ttu-id="c1e2c-119">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c1e2c-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c1e2c-120">\_如果沒有任何屬性值可供使用，則傳回 FALSE，否則傳回 s \_ OK 或 standard COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e2c-121">備註</span><span class="sxs-lookup"><span data-stu-id="c1e2c-121">Remarks</span></span>

<span data-ttu-id="c1e2c-122">每個值的類型都必須與呼叫 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)時所設定的類型相同。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="c1e2c-123">在陣列中， *pid* 指向的每個值是其中一個 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="c1e2c-124">您可以擴充此識別系統。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-124">You can extend this identification system.</span></span> <span data-ttu-id="c1e2c-125">請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="c1e2c-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e2c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1e2c-126">Requirements</span></span>



| <span data-ttu-id="c1e2c-127">需求</span><span class="sxs-lookup"><span data-stu-id="c1e2c-127">Requirement</span></span> | <span data-ttu-id="c1e2c-128">值</span><span class="sxs-lookup"><span data-stu-id="c1e2c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e2c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1e2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e2c-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e2c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c1e2c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1e2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e2c-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e2c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1e2c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c1e2c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e2c-134"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e2c-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="c1e2c-135">Idl</span><span class="sxs-lookup"><span data-stu-id="c1e2c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1e2c-136"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1e2c-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e2c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1e2c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e2c-138">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="c1e2c-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="c1e2c-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="c1e2c-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1e2c-140">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="c1e2c-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="c1e2c-141">WIA 屬性常數</span><span class="sxs-lookup"><span data-stu-id="c1e2c-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="c1e2c-142">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="c1e2c-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
