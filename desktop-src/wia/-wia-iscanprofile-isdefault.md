---
description: 取得值，這個值會指出設定檔是否為相關聯之 IWiaItem2 裝置的預設掃描設定檔。
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'IScanProfile：： IsDefault 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943585"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="c6455-103">IScanProfile：： IsDefault 方法</span><span class="sxs-lookup"><span data-stu-id="c6455-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="c6455-104">取得值，這個值會指出設定檔是否為相關聯之 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置的預設掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="c6455-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6455-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6455-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="c6455-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6455-107">*pbDefault* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6455-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6455-108">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="c6455-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c6455-109">_ \* BOOL \* \* 的指標。</span><span class="sxs-lookup"><span data-stu-id="c6455-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c6455-110"><span id="TRUE"></span><span id="true"></span>**真**</span><span class="sxs-lookup"><span data-stu-id="c6455-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="c6455-111">設定檔是預設值。</span><span class="sxs-lookup"><span data-stu-id="c6455-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c6455-112"><span id="FALSE"></span><span id="false"></span>**假**</span><span class="sxs-lookup"><span data-stu-id="c6455-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="c6455-113">設定檔不是預設值。</span><span class="sxs-lookup"><span data-stu-id="c6455-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6455-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6455-114">Return value</span></span>

<span data-ttu-id="c6455-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6455-115">Type: **HRESULT**</span></span>

<span data-ttu-id="c6455-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c6455-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6455-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6455-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6455-118">備註</span><span class="sxs-lookup"><span data-stu-id="c6455-118">Remarks</span></span>

<span data-ttu-id="c6455-119">如果設定檔包含元素，則 *pbDefault* 為 **TRUE** `<Default>` 。</span><span class="sxs-lookup"><span data-stu-id="c6455-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="c6455-120">如果沒有這樣的元素，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c6455-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="c6455-121">元素沒有值。</span><span class="sxs-lookup"><span data-stu-id="c6455-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6455-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6455-122">Requirements</span></span>



| <span data-ttu-id="c6455-123">需求</span><span class="sxs-lookup"><span data-stu-id="c6455-123">Requirement</span></span> | <span data-ttu-id="c6455-124">值</span><span class="sxs-lookup"><span data-stu-id="c6455-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6455-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6455-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6455-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6455-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c6455-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6455-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6455-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6455-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6455-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c6455-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6455-130"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6455-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="c6455-131">Idl</span><span class="sxs-lookup"><span data-stu-id="c6455-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6455-132"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6455-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6455-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6455-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6455-134">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="c6455-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="c6455-135">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="c6455-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




