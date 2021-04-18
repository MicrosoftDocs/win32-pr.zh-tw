---
description: PatchProperty 屬性會取得套用至特定產品實例之特定修補程式的相關資訊。 這個屬性會呼叫 MsiGetPatchInfoEx。
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: PatchProperty 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976130"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="9d5c2-104">PatchProperty 方法</span><span class="sxs-lookup"><span data-stu-id="9d5c2-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="9d5c2-105">**PatchProperty** 屬性會取得套用至特定產品實例之特定修補程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="9d5c2-106">這個屬性會呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d5c2-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="9d5c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d5c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5c2-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="9d5c2-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5c2-110">*SzProperty* 參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="9d5c2-111">Name</span><span class="sxs-lookup"><span data-stu-id="9d5c2-111">Name</span></span>          | <span data-ttu-id="9d5c2-112">意義</span><span class="sxs-lookup"><span data-stu-id="9d5c2-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5c2-113">LocalPackage</span><span class="sxs-lookup"><span data-stu-id="9d5c2-113">LocalPackage</span></span>  | <span data-ttu-id="9d5c2-114">取得產品所使用的快取修補檔案。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9d5c2-115">轉換</span><span class="sxs-lookup"><span data-stu-id="9d5c2-115">Transforms</span></span>    | <span data-ttu-id="9d5c2-116">取得上次修補安裝所套用至產品的一組修補程式轉換。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="9d5c2-117">如果使用者未登入電腦，則每個使用者非受控應用程式可能無法使用此值。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="9d5c2-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="9d5c2-118">InstallDate</span></span>   | <span data-ttu-id="9d5c2-119">取得修補程式套用至產品的日期。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9d5c2-120">可卸載</span><span class="sxs-lookup"><span data-stu-id="9d5c2-120">Uninstallable</span></span> | <span data-ttu-id="9d5c2-121">如果修補程式標示為可以從產品卸載，則會傳回 "1"。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="9d5c2-122">在此情況下，如果另一個無法卸載的修補程式需要此修補程式，則安裝程式仍然可以封鎖卸載。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="9d5c2-123">狀態</span><span class="sxs-lookup"><span data-stu-id="9d5c2-123">State</span></span>         | <span data-ttu-id="9d5c2-124">如果此修補程式目前套用至產品，則會傳回 "1"。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="9d5c2-125">如果已由另一個修補程式取代此修補程式，則會傳回 "2"。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="9d5c2-126">如果此修補程式已由另一個修補程式淘汰，則會傳回 "4"。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="9d5c2-127">這些值會對應至 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)的 *dwFilter* 參數所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="9d5c2-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="9d5c2-128">DisplayName</span></span>   | <span data-ttu-id="9d5c2-129">取得修補程式的註冊顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="9d5c2-130">針對未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含 DisplayName 屬性的修補程式，傳回的顯示名稱為空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="9d5c2-131">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="9d5c2-131">MoreInfoURL</span></span>   | <span data-ttu-id="9d5c2-132">取得修補程式的已註冊支援資訊 URL。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="9d5c2-133">針對未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含 MoreInfoURL 屬性的修補程式，傳回的支援資訊 URL 是 ( "" ) 的空字串。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5c2-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d5c2-134">Return value</span></span>

<span data-ttu-id="9d5c2-135">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5c2-136">備註</span><span class="sxs-lookup"><span data-stu-id="9d5c2-136">Remarks</span></span>

<span data-ttu-id="9d5c2-137">\_ \_ 如果 [**修補程式**](patch-object.md)物件是以空字串來初始化， 則這個方法可能會傳回錯誤未知的修補程式。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5c2-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d5c2-138">Requirements</span></span>



| <span data-ttu-id="9d5c2-139">需求</span><span class="sxs-lookup"><span data-stu-id="9d5c2-139">Requirement</span></span> | <span data-ttu-id="9d5c2-140">值</span><span class="sxs-lookup"><span data-stu-id="9d5c2-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5c2-141">版本</span><span class="sxs-lookup"><span data-stu-id="9d5c2-141">Version</span></span><br/> | <span data-ttu-id="9d5c2-142">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d5c2-143">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9d5c2-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d5c2-144">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9d5c2-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9d5c2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9d5c2-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d5c2-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d5c2-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9d5c2-147">IID</span><span class="sxs-lookup"><span data-stu-id="9d5c2-147">IID</span></span><br/>     | <span data-ttu-id="9d5c2-148">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9d5c2-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9d5c2-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d5c2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5c2-150">**Patch**</span><span class="sxs-lookup"><span data-stu-id="9d5c2-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="9d5c2-151">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="9d5c2-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="9d5c2-152">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="9d5c2-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="9d5c2-153">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="9d5c2-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




