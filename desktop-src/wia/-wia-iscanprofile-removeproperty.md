---
description: 在中移除指定的子屬性清單 <Properties> 掃描設定檔的元素。
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile：： RemoveProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113909"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="712b0-104">IScanProfile：： RemoveProperty 方法</span><span class="sxs-lookup"><span data-stu-id="712b0-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="712b0-105">在掃描設定檔的元素中移除指定的子屬性清單 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="712b0-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="712b0-106">語法</span><span class="sxs-lookup"><span data-stu-id="712b0-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="712b0-107">參數</span><span class="sxs-lookup"><span data-stu-id="712b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712b0-108">*num* \[在\]</span><span class="sxs-lookup"><span data-stu-id="712b0-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="712b0-109">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="712b0-109">Type: **ULONG**</span></span>

<span data-ttu-id="712b0-110">由 *pid* 指向之陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="712b0-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="712b0-111">*pid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="712b0-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="712b0-112">類型： \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="712b0-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="712b0-113">要刪除之屬性識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="712b0-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="712b0-114">每個都是 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="712b0-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712b0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="712b0-115">Return value</span></span>

<span data-ttu-id="712b0-116">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="712b0-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="712b0-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="712b0-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="712b0-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="712b0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="712b0-119">備註</span><span class="sxs-lookup"><span data-stu-id="712b0-119">Remarks</span></span>

<span data-ttu-id="712b0-120">在陣列中， *pid* 指向的每個值是其中一個 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="712b0-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="712b0-121">您可以擴充此識別系統。</span><span class="sxs-lookup"><span data-stu-id="712b0-121">You can extend this identification system.</span></span> <span data-ttu-id="712b0-122">請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="712b0-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="712b0-123">設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="712b0-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="712b0-124">如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="712b0-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="712b0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="712b0-125">Requirements</span></span>



| <span data-ttu-id="712b0-126">需求</span><span class="sxs-lookup"><span data-stu-id="712b0-126">Requirement</span></span> | <span data-ttu-id="712b0-127">值</span><span class="sxs-lookup"><span data-stu-id="712b0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="712b0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="712b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="712b0-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="712b0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="712b0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="712b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="712b0-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="712b0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="712b0-132">標頭</span><span class="sxs-lookup"><span data-stu-id="712b0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="712b0-133"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="712b0-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="712b0-134">Idl</span><span class="sxs-lookup"><span data-stu-id="712b0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="712b0-135"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="712b0-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712b0-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="712b0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712b0-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="712b0-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="712b0-138">**概念**</span><span class="sxs-lookup"><span data-stu-id="712b0-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="712b0-139">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="712b0-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="712b0-140">WIA 屬性常數</span><span class="sxs-lookup"><span data-stu-id="712b0-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="712b0-141">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="712b0-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




