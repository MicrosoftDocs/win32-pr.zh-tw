---
description: IScanProfile 介面代表單一掃描設定檔，可讓應用程式設定和取得設定檔的屬性。
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: IScanProfile 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977055"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="a9c89-103">IScanProfile 介面</span><span class="sxs-lookup"><span data-stu-id="a9c89-103">IScanProfile interface</span></span>

<span data-ttu-id="a9c89-104">**IScanProfile** 介面代表單一掃描設定檔，可讓應用程式設定和取得設定檔的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9c89-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="a9c89-105">成員</span><span class="sxs-lookup"><span data-stu-id="a9c89-105">Members</span></span>

<span data-ttu-id="a9c89-106">**IScanProfile** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="a9c89-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a9c89-107">**IScanProfile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9c89-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="a9c89-108">方法</span><span class="sxs-lookup"><span data-stu-id="a9c89-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9c89-109">方法</span><span class="sxs-lookup"><span data-stu-id="a9c89-109">Methods</span></span>

<span data-ttu-id="a9c89-110">**IScanProfile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a9c89-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="a9c89-111">方法</span><span class="sxs-lookup"><span data-stu-id="a9c89-111">Method</span></span>                                                     | <span data-ttu-id="a9c89-112">描述</span><span class="sxs-lookup"><span data-stu-id="a9c89-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9c89-113">**GetAllPropIDs**</span><span class="sxs-lookup"><span data-stu-id="a9c89-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="a9c89-114">取得設定檔中的所有可用屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9c89-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="a9c89-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a9c89-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="a9c89-116">傳回裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9c89-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="a9c89-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="a9c89-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="a9c89-118">傳回設定檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a9c89-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a9c89-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="a9c89-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="a9c89-120">取得與設定檔相關聯之 WIA 2.0 專案類別目錄的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a9c89-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="a9c89-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a9c89-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="a9c89-122">取得設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c89-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a9c89-123">**GetNumPropIDS**</span><span class="sxs-lookup"><span data-stu-id="a9c89-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="a9c89-124">取得設定檔中的屬性識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="a9c89-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="a9c89-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="a9c89-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="a9c89-126">取得掃描設定檔的元素中指定之子屬性的值 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="a9c89-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="a9c89-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="a9c89-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="a9c89-128">取得值，這個值會指出設定檔是否為相關聯之 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置的預設掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9c89-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="a9c89-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="a9c89-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="a9c89-130">在掃描設定檔的元素中移除指定的子屬性清單 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="a9c89-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="a9c89-131">**儲存**</span><span class="sxs-lookup"><span data-stu-id="a9c89-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="a9c89-132">將設定檔的變更儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="a9c89-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="a9c89-133">**SetItem**</span><span class="sxs-lookup"><span data-stu-id="a9c89-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="a9c89-134">設定與設定檔相關聯之 WIA 2.0 專案類別目錄的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a9c89-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="a9c89-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a9c89-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="a9c89-136">設定設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c89-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a9c89-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="a9c89-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="a9c89-138">在掃描設定檔的元素中，設定指定之子屬性的值 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="a9c89-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="a9c89-139">備註</span><span class="sxs-lookup"><span data-stu-id="a9c89-139">Remarks</span></span>

<span data-ttu-id="a9c89-140">任何 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置都可以有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9c89-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="a9c89-141">不過，  [WIA \_ 類別目錄 \_ 已完成檔案] 和 [wia 類別根目錄] 類型的 IWiaItem2 專案 \_ \_ \_ 不能有設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9c89-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="a9c89-142">如果使用 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法儲存掃描設定檔，它會儲存為 XML 檔案，位於% USERPROFILE% 的 \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles。</span><span class="sxs-lookup"><span data-stu-id="a9c89-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="a9c89-143">若要建立 **IScanProfile** 物件的實例，請使用 [**IScanProfileMgr：： CreateProfile**](-wia-iscanprofilemgr-createprofile.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a9c89-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="a9c89-144">若要取得已儲存至磁片的掃描設定檔的參考，請使用 [**IScanProfileMgr：： OpenProfile**](-wia-iscanprofilemgr-openprofile.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a9c89-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="a9c89-145">所有掃描設定檔都有下列元素： `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` 、和 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="a9c89-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="a9c89-146">裝置的預設設定檔也有一個 `<Default>` 元素。</span><span class="sxs-lookup"><span data-stu-id="a9c89-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="a9c89-147">`<ProfileGUID>` `<DeviceID>` 建立設定檔之後，就無法變更和元素。</span><span class="sxs-lookup"><span data-stu-id="a9c89-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="a9c89-148">在 `<ProfileName>` `<WiaItem>` 建立設定檔之後，可以變更元素和元素的值。</span><span class="sxs-lookup"><span data-stu-id="a9c89-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="a9c89-149">您 `<Default>` 可以新增或刪除元素。</span><span class="sxs-lookup"><span data-stu-id="a9c89-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="a9c89-150">您可以使用 [**IScanProfile：： SetName**](-wia-iscanprofile-setname.md)、 [**IScanProfile：： SetItem**](-wia-iscanprofile-setitem.md)和 [**IScanProfileMgr：： SetDefault**](-wia-iscanprofilemgr-setdefault.md) 方法以程式設計方式完成此動作。</span><span class="sxs-lookup"><span data-stu-id="a9c89-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="a9c89-151">使用者也可以透過 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法變更這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a9c89-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="a9c89-152">`<Properties>`元素包含 `<Property>` 子系。</span><span class="sxs-lookup"><span data-stu-id="a9c89-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="a9c89-153">使用這些專案，將任何 WIA 2.0 專案或裝置屬性新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9c89-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="a9c89-154">您也可以開發自己的映射獲取 `<Property>` 子系。</span><span class="sxs-lookup"><span data-stu-id="a9c89-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="a9c89-155">這可延伸掃描設定檔架構。</span><span class="sxs-lookup"><span data-stu-id="a9c89-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="a9c89-156"> (如需延伸架構的詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)、 [**IScanProfile：： GetProperty**](-wia-iscanprofile-getproperty.md)和 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a9c89-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c89-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9c89-157">Requirements</span></span>



| <span data-ttu-id="a9c89-158">需求</span><span class="sxs-lookup"><span data-stu-id="a9c89-158">Requirement</span></span> | <span data-ttu-id="a9c89-159">值</span><span class="sxs-lookup"><span data-stu-id="a9c89-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c89-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9c89-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c89-161">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c89-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a9c89-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9c89-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c89-163">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c89-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9c89-164">Idl</span><span class="sxs-lookup"><span data-stu-id="a9c89-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9c89-165"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9c89-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c89-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9c89-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c89-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a9c89-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a9c89-168">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="a9c89-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
