---
description: 將設定檔的變更儲存至磁片。
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile：： Save 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512052"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="8004c-103">IScanProfile：： Save 方法</span><span class="sxs-lookup"><span data-stu-id="8004c-103">IScanProfile::Save method</span></span>

<span data-ttu-id="8004c-104">將設定檔的變更儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="8004c-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="8004c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8004c-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="8004c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8004c-106">Parameters</span></span>

<span data-ttu-id="8004c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8004c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8004c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8004c-108">Return value</span></span>

<span data-ttu-id="8004c-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8004c-109">Type: **HRESULT**</span></span>

<span data-ttu-id="8004c-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8004c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8004c-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8004c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8004c-112">備註</span><span class="sxs-lookup"><span data-stu-id="8004c-112">Remarks</span></span>

<span data-ttu-id="8004c-113">儲存的掃描設定檔是儲存在% USERPROFILE% \\ Application Data \\ Microsoft \\ Document CENTER UserScanProfiles 的 XML 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="8004c-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="8004c-114">如果有一個以上的進程寫入 [**IScanProfile**](-wia-iscanprofile.md) 物件，則呼叫 **IScanProfile：： Save** last 的進程是唯一儲存變更的進程。</span><span class="sxs-lookup"><span data-stu-id="8004c-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="8004c-115">**IScanProfile：： Save** 方法會先驗證設定檔，然後再儲存。</span><span class="sxs-lookup"><span data-stu-id="8004c-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="8004c-116">設定檔一律會被視為有效，除非與設定檔相關聯的 Windows 映像取得 (WIA) 2.0 專案的分類為 [WIA \_ 類別] \_ 或 [wia \_ 類別 \_ 送紙器]。</span><span class="sxs-lookup"><span data-stu-id="8004c-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="8004c-117">如果分類為 [WIA \_ 類別] \_ 或 \_ [wia 類別]，則 \_ 如果屬性包含在設定檔中，則下列屬性必須對專案有效：</span><span class="sxs-lookup"><span data-stu-id="8004c-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="8004c-118">WIA \_ IP \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="8004c-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="8004c-119">WIA \_ IP \_ 對比</span><span class="sxs-lookup"><span data-stu-id="8004c-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="8004c-120">WIA \_ IPA \_ 資料類型</span><span class="sxs-lookup"><span data-stu-id="8004c-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="8004c-121">WIA \_ IP \_ XRES</span><span class="sxs-lookup"><span data-stu-id="8004c-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="8004c-122">WIA \_ IPA \_ 格式</span><span class="sxs-lookup"><span data-stu-id="8004c-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="8004c-123">此外，如果類別是 WIA \_ 類別 \_ 送紙器，則 [wia \_ ip \_ 頁面大小] \_ 屬性必須是有效的，如果設定檔中有此屬性的話。</span><span class="sxs-lookup"><span data-stu-id="8004c-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="8004c-124">如需這些屬性的詳細資訊，請參閱 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md)。</span><span class="sxs-lookup"><span data-stu-id="8004c-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8004c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8004c-125">Requirements</span></span>



| <span data-ttu-id="8004c-126">需求</span><span class="sxs-lookup"><span data-stu-id="8004c-126">Requirement</span></span> | <span data-ttu-id="8004c-127">值</span><span class="sxs-lookup"><span data-stu-id="8004c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8004c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8004c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8004c-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8004c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8004c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8004c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8004c-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8004c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8004c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8004c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8004c-133"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="8004c-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="8004c-134">Idl</span><span class="sxs-lookup"><span data-stu-id="8004c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8004c-135"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8004c-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8004c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8004c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8004c-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="8004c-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="8004c-138">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="8004c-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




