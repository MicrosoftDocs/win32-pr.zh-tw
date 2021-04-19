---
description: IScanProfileMgr 介面提供建立、開啟、刪除及管理掃描設定檔的方法。
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: 'IScanProfileMgr 介面 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972267"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="eb2ba-103">IScanProfileMgr 介面</span><span class="sxs-lookup"><span data-stu-id="eb2ba-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="eb2ba-104">**IScanProfileMgr** 介面提供建立、開啟、刪除及管理掃描設定檔的方法。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="eb2ba-105">成員</span><span class="sxs-lookup"><span data-stu-id="eb2ba-105">Members</span></span>

<span data-ttu-id="eb2ba-106">**IScanProfileMgr** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eb2ba-107">**IScanProfileMgr** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb2ba-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="eb2ba-108">方法</span><span class="sxs-lookup"><span data-stu-id="eb2ba-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb2ba-109">方法</span><span class="sxs-lookup"><span data-stu-id="eb2ba-109">Methods</span></span>

<span data-ttu-id="eb2ba-110">**IScanProfileMgr** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="eb2ba-111">方法</span><span class="sxs-lookup"><span data-stu-id="eb2ba-111">Method</span></span>                                                                              | <span data-ttu-id="eb2ba-112">描述</span><span class="sxs-lookup"><span data-stu-id="eb2ba-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb2ba-113">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="eb2ba-114">建立空的掃描設定檔，並將它與掃描器或其他 WIA 2.0 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="eb2ba-115">**DeleteAllProfiles**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="eb2ba-116">刪除與指定裝置相關聯的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="eb2ba-117">**DeleteAllProfilesForUser**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="eb2ba-118">刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="eb2ba-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="eb2ba-120">刪除指定的掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="eb2ba-121">**GetDefaultProfile**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="eb2ba-122">取得預設掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="eb2ba-123">**GetNumProfiles**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="eb2ba-124">取得在您的應用程式執行所在系統中為使用者建立的掃描設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="eb2ba-125">**GetNumProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="eb2ba-126">取得裝置的掃描設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="eb2ba-127">**>ipartner.getprofiles**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="eb2ba-128">取得您的應用程式執行所在系統中使用者可用的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="eb2ba-129">**GetProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="eb2ba-130">取得與裝置相關聯的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="eb2ba-131">**OpenProfile**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="eb2ba-132">開啟已儲存至磁片的掃描設定檔做為 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="eb2ba-133">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="eb2ba-134">重新列舉系統中的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="eb2ba-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="eb2ba-136">將指定的掃描設定檔設定為預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="eb2ba-137">備註</span><span class="sxs-lookup"><span data-stu-id="eb2ba-137">Remarks</span></span>

<span data-ttu-id="eb2ba-138">若要建立 **IScanProfileMgr** 物件，請使用具有下列參數的 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法：</span><span class="sxs-lookup"><span data-stu-id="eb2ba-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="eb2ba-139">如果使用 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法儲存掃描設定檔，它會儲存為 XML 檔案，位於% USERPROFILE% 的 \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles。</span><span class="sxs-lookup"><span data-stu-id="eb2ba-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb2ba-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb2ba-140">Requirements</span></span>



| <span data-ttu-id="eb2ba-141">需求</span><span class="sxs-lookup"><span data-stu-id="eb2ba-141">Requirement</span></span> | <span data-ttu-id="eb2ba-142">值</span><span class="sxs-lookup"><span data-stu-id="eb2ba-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2ba-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb2ba-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2ba-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb2ba-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eb2ba-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb2ba-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2ba-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb2ba-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb2ba-147">標頭</span><span class="sxs-lookup"><span data-stu-id="eb2ba-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb2ba-148"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb2ba-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="eb2ba-149">Idl</span><span class="sxs-lookup"><span data-stu-id="eb2ba-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb2ba-150"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb2ba-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb2ba-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb2ba-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2ba-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eb2ba-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="eb2ba-153">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="eb2ba-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
