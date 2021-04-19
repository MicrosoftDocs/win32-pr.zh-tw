---
description: Product 物件代表產品的唯一實例，也就是已公告、已安裝或未知。您可以使用 Product 屬性將物件具現化為 &\# 0034;WindowsInstaller： Product (ProductCode，UserSid，CoNtext) &\# 0034;。
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982978"
---
# <a name="product-object"></a><span data-ttu-id="c1d88-103">Product 物件</span><span class="sxs-lookup"><span data-stu-id="c1d88-103">Product object</span></span>

<span data-ttu-id="c1d88-104">**Product** 物件代表產品的唯一實例，也就是已公告、已安裝或未知。</span><span class="sxs-lookup"><span data-stu-id="c1d88-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="c1d88-105">您可以使用 **product** 屬性將物件具現化為 "WindowsInstaller"、" (*"、*" *UserSid*"、 *CoNtext*) "。</span><span class="sxs-lookup"><span data-stu-id="c1d88-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="c1d88-106">每一機器內容的 *UserSid* 必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="c1d88-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="c1d88-107">當內容不是每一部電腦時， *UserSid* 可為指定目前使用者的 null。</span><span class="sxs-lookup"><span data-stu-id="c1d88-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="c1d88-108">需要 *ProductCode* 和 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="c1d88-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="c1d88-109">成員</span><span class="sxs-lookup"><span data-stu-id="c1d88-109">Members</span></span>

<span data-ttu-id="c1d88-110">**Product** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c1d88-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="c1d88-111">方法</span><span class="sxs-lookup"><span data-stu-id="c1d88-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1d88-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c1d88-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1d88-113">方法</span><span class="sxs-lookup"><span data-stu-id="c1d88-113">Methods</span></span>

<span data-ttu-id="c1d88-114">**Product** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c1d88-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="c1d88-115">方法</span><span class="sxs-lookup"><span data-stu-id="c1d88-115">Method</span></span>                                                                 | <span data-ttu-id="c1d88-116">描述</span><span class="sxs-lookup"><span data-stu-id="c1d88-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1d88-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="c1d88-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="c1d88-118">將磁片新增至已註冊的磁片集。</span><span class="sxs-lookup"><span data-stu-id="c1d88-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="c1d88-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="c1d88-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="c1d88-120">將網路或 URL 來源新增至來源清單。</span><span class="sxs-lookup"><span data-stu-id="c1d88-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="c1d88-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="c1d88-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="c1d88-122">清除指定類型來源的完整來源清單。</span><span class="sxs-lookup"><span data-stu-id="c1d88-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="c1d88-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="c1d88-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="c1d88-124">從來源清單中移除已註冊磁片集的磁片。</span><span class="sxs-lookup"><span data-stu-id="c1d88-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="c1d88-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="c1d88-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="c1d88-126">從來源清單中移除網路或 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="c1d88-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="c1d88-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="c1d88-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="c1d88-128">清除上次使用的來源。</span><span class="sxs-lookup"><span data-stu-id="c1d88-128">Clears the last used source.</span></span> <span data-ttu-id="c1d88-129">這會在下一次需要來源時強制來源清單解析。</span><span class="sxs-lookup"><span data-stu-id="c1d88-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c1d88-130">屬性</span><span class="sxs-lookup"><span data-stu-id="c1d88-130">Properties</span></span>

<span data-ttu-id="c1d88-131">**Product** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d88-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="c1d88-132">屬性</span><span class="sxs-lookup"><span data-stu-id="c1d88-132">Property</span></span>                                                      | <span data-ttu-id="c1d88-133">描述</span><span class="sxs-lookup"><span data-stu-id="c1d88-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1d88-134">**ComponentState**</span><span class="sxs-lookup"><span data-stu-id="c1d88-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="c1d88-135">此產品實例之指定元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1d88-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="c1d88-136">**Context**</span><span class="sxs-lookup"><span data-stu-id="c1d88-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="c1d88-137">此產品實例的內容，做為 MSIINSTALLCONTEXT 值。</span><span class="sxs-lookup"><span data-stu-id="c1d88-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="c1d88-138">**FeatureState**</span><span class="sxs-lookup"><span data-stu-id="c1d88-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="c1d88-139">此產品實例之指定功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="c1d88-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="c1d88-140">**InstallProperty**</span><span class="sxs-lookup"><span data-stu-id="c1d88-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="c1d88-141">指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c1d88-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="c1d88-142">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="c1d88-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="c1d88-143">列舉此產品實例的所有媒體磁片。</span><span class="sxs-lookup"><span data-stu-id="c1d88-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="c1d88-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c1d88-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="c1d88-145">傳回產品代碼。</span><span class="sxs-lookup"><span data-stu-id="c1d88-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="c1d88-146">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d88-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="c1d88-147">取得和設定來源資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d88-147">Get and set the source information properties.</span></span> <span data-ttu-id="c1d88-148">這是讀取或寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d88-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="c1d88-149">**來源**</span><span class="sxs-lookup"><span data-stu-id="c1d88-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="c1d88-150">列舉此產品實例的所有來源。</span><span class="sxs-lookup"><span data-stu-id="c1d88-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="c1d88-151">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c1d88-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="c1d88-152">產品的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="c1d88-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="c1d88-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="c1d88-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="c1d88-154">傳回使用者 SID，此為此產品實例可用的帳戶。</span><span class="sxs-lookup"><span data-stu-id="c1d88-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="c1d88-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1d88-155">Requirements</span></span>



| <span data-ttu-id="c1d88-156">需求</span><span class="sxs-lookup"><span data-stu-id="c1d88-156">Requirement</span></span> | <span data-ttu-id="c1d88-157">值</span><span class="sxs-lookup"><span data-stu-id="c1d88-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d88-158">版本</span><span class="sxs-lookup"><span data-stu-id="c1d88-158">Version</span></span><br/> | <span data-ttu-id="c1d88-159">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c1d88-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1d88-160">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c1d88-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1d88-161">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1d88-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c1d88-162">DLL</span><span class="sxs-lookup"><span data-stu-id="c1d88-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1d88-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1d88-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c1d88-164">IID</span><span class="sxs-lookup"><span data-stu-id="c1d88-164">IID</span></span><br/>     | <span data-ttu-id="c1d88-165">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c1d88-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c1d88-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1d88-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d88-167">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="c1d88-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




