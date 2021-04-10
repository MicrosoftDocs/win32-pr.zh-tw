---
description: 設定指定之子屬性的值。 <Properties> 掃描設定檔的元素。
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile：： SetProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691104"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="e7893-104">IScanProfile：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="e7893-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="e7893-105">在掃描設定檔的元素中，設定指定之子屬性的值 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="e7893-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7893-106">語法</span><span class="sxs-lookup"><span data-stu-id="e7893-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="e7893-107">參數</span><span class="sxs-lookup"><span data-stu-id="e7893-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7893-108">*num* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7893-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7893-109">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="e7893-109">Type: **ULONG**</span></span>

<span data-ttu-id="e7893-110">由 *pid* 和 *pvar* 指向的陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="e7893-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="e7893-111">*pid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7893-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7893-112">類型： \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="e7893-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="e7893-113">要設定之屬性識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="e7893-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="e7893-114">陣列中的每個值都是 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e7893-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7893-115">_pvar \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7893-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7893-116">類型： \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="e7893-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="e7893-117">要指派給屬性之值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="e7893-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7893-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7893-118">Return value</span></span>

<span data-ttu-id="e7893-119">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e7893-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e7893-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e7893-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7893-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e7893-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7893-122">備註</span><span class="sxs-lookup"><span data-stu-id="e7893-122">Remarks</span></span>

<span data-ttu-id="e7893-123">在陣列中， *pid* 指向的每個值是其中一個 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e7893-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="e7893-124">您可以擴充此識別系統。</span><span class="sxs-lookup"><span data-stu-id="e7893-124">You can extend this identification system.</span></span> <span data-ttu-id="e7893-125">請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="e7893-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="e7893-126">設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="e7893-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="e7893-127">如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="e7893-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7893-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7893-128">Requirements</span></span>



| <span data-ttu-id="e7893-129">需求</span><span class="sxs-lookup"><span data-stu-id="e7893-129">Requirement</span></span> | <span data-ttu-id="e7893-130">值</span><span class="sxs-lookup"><span data-stu-id="e7893-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7893-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7893-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e7893-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7893-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e7893-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7893-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e7893-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7893-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7893-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e7893-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7893-136"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7893-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="e7893-137">Idl</span><span class="sxs-lookup"><span data-stu-id="e7893-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7893-138"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7893-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7893-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7893-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7893-140">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="e7893-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="e7893-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="e7893-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e7893-142">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="e7893-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="e7893-143">WIA 屬性常數</span><span class="sxs-lookup"><span data-stu-id="e7893-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="e7893-144">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="e7893-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
