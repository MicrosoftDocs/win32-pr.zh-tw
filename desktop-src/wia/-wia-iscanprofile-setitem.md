---
description: 設定與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'IScanProfile：： SetItem 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996607"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="a4643-103">IScanProfile：： SetItem 方法</span><span class="sxs-lookup"><span data-stu-id="a4643-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="a4643-104">設定與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="a4643-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4643-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4643-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="a4643-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4643-107">*guidCategory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4643-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4643-108">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="a4643-108">Type: **GUID**</span></span>

<span data-ttu-id="a4643-109">WIA 2.0 專案分類的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a4643-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="a4643-110">這必須是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。</span><span class="sxs-lookup"><span data-stu-id="a4643-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4643-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4643-111">Return value</span></span>

<span data-ttu-id="a4643-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a4643-112">Type: **HRESULT**</span></span>

<span data-ttu-id="a4643-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a4643-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4643-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a4643-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4643-115">備註</span><span class="sxs-lookup"><span data-stu-id="a4643-115">Remarks</span></span>

<span data-ttu-id="a4643-116">使用者可以使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更類別。</span><span class="sxs-lookup"><span data-stu-id="a4643-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="a4643-117">設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="a4643-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="a4643-118">如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="a4643-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4643-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4643-119">Requirements</span></span>



| <span data-ttu-id="a4643-120">需求</span><span class="sxs-lookup"><span data-stu-id="a4643-120">Requirement</span></span> | <span data-ttu-id="a4643-121">值</span><span class="sxs-lookup"><span data-stu-id="a4643-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4643-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4643-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a4643-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4643-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a4643-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4643-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a4643-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4643-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4643-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a4643-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4643-127"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4643-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="a4643-128">Idl</span><span class="sxs-lookup"><span data-stu-id="a4643-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4643-129"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4643-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4643-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4643-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4643-131">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="a4643-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="a4643-132">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="a4643-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




