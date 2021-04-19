---
description: 取得與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile：： GetItem 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001344"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="aae5b-103">IScanProfile：： GetItem 方法</span><span class="sxs-lookup"><span data-stu-id="aae5b-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="aae5b-104">取得與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="aae5b-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae5b-105">語法</span><span class="sxs-lookup"><span data-stu-id="aae5b-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="aae5b-106">參數</span><span class="sxs-lookup"><span data-stu-id="aae5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae5b-107">*pguidCategory* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aae5b-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae5b-108">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="aae5b-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="aae5b-109">WIA 2.0 專案分類的 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="aae5b-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="aae5b-110">這一律是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。</span><span class="sxs-lookup"><span data-stu-id="aae5b-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae5b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aae5b-111">Return value</span></span>

<span data-ttu-id="aae5b-112">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="aae5b-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="aae5b-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="aae5b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aae5b-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aae5b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae5b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aae5b-115">Requirements</span></span>



| <span data-ttu-id="aae5b-116">需求</span><span class="sxs-lookup"><span data-stu-id="aae5b-116">Requirement</span></span> | <span data-ttu-id="aae5b-117">值</span><span class="sxs-lookup"><span data-stu-id="aae5b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae5b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aae5b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aae5b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aae5b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="aae5b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aae5b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aae5b-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aae5b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aae5b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aae5b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae5b-123"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="aae5b-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="aae5b-124">Idl</span><span class="sxs-lookup"><span data-stu-id="aae5b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aae5b-125"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="aae5b-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae5b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aae5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae5b-127">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="aae5b-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="aae5b-128">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="aae5b-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




