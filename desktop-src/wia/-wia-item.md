---
description: Windows 映像取得 (WIA) 硬體裝置會以專案物件的階層樹狀結構表示。 此樹狀結構中的根專案代表裝置本身，而子專案代表影像、資料夾或掃描張床。
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Item 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691100"
---
# <a name="item-object"></a><span data-ttu-id="9ae81-104">Item 物件</span><span class="sxs-lookup"><span data-stu-id="9ae81-104">Item object</span></span>

<span data-ttu-id="9ae81-105">Windows 映像取得 (WIA) 硬體裝置會以 **專案** 物件的階層樹狀結構表示。</span><span class="sxs-lookup"><span data-stu-id="9ae81-105">Windows Image Acquisition (WIA) hardware devices are represented as hierarchical trees of **Item** objects.</span></span> <span data-ttu-id="9ae81-106">此樹狀結構中的根專案代表裝置本身，而子專案代表影像、資料夾或掃描張床。</span><span class="sxs-lookup"><span data-stu-id="9ae81-106">The root item in this tree represents the device itself, while child items represent images, folders, or scanning beds.</span></span>

<span data-ttu-id="9ae81-107">使用 **Item** 物件將資料傳輸至檔案、流覽特定裝置的專案樹狀結構，或取得影像或裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ae81-107">Use the **Item** object to transfer data to a file, to navigate the item tree for a particular device, or to retrieve information about an image or a device.</span></span>

## <a name="members"></a><span data-ttu-id="9ae81-108">成員</span><span class="sxs-lookup"><span data-stu-id="9ae81-108">Members</span></span>

<span data-ttu-id="9ae81-109">**Item** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9ae81-109">The **Item** object has these types of members:</span></span>

-   [<span data-ttu-id="9ae81-110">方法</span><span class="sxs-lookup"><span data-stu-id="9ae81-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ae81-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae81-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ae81-112">方法</span><span class="sxs-lookup"><span data-stu-id="9ae81-112">Methods</span></span>

<span data-ttu-id="9ae81-113">**Item** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9ae81-113">The **Item** object has these methods.</span></span>



| <span data-ttu-id="9ae81-114">方法</span><span class="sxs-lookup"><span data-stu-id="9ae81-114">Method</span></span>                                                         | <span data-ttu-id="9ae81-115">描述</span><span class="sxs-lookup"><span data-stu-id="9ae81-115">Description</span></span>                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ae81-116">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="9ae81-116">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md) | <span data-ttu-id="9ae81-117">**Item** 物件的 [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。</span><span class="sxs-lookup"><span data-stu-id="9ae81-117">The [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) method of the **Item** object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span><br/>                                                                     |
| [<span data-ttu-id="9ae81-118">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="9ae81-118">**GetPropById**</span></span>](-wia-iwiadispatchitem-getpropbyid.md)       | <span data-ttu-id="9ae81-119">**Item** 物件的 [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)方法會使用 item 屬性的 ID 來傳回其值。</span><span class="sxs-lookup"><span data-stu-id="9ae81-119">The [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) method of the **Item** object uses the ID of an item property to return its value.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="9ae81-120">**TakePicture**</span><span class="sxs-lookup"><span data-stu-id="9ae81-120">**TakePicture**</span></span>](-wia-iwiadispatchitem-takepicture.md)       | <span data-ttu-id="9ae81-121">**Item** 物件的 [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的 **專案** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ae81-121">The [**TakePicture**](-wia-iwiadispatchitem-takepicture.md) method of the **Item** object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="9ae81-122">此方法僅適用于數位相機裝置。</span><span class="sxs-lookup"><span data-stu-id="9ae81-122">This method applies only to digital camera devices.</span></span><br/> |
| [<span data-ttu-id="9ae81-123">**傳送**</span><span class="sxs-lookup"><span data-stu-id="9ae81-123">**Transfer**</span></span>](-wia-iwiadispatchitem-transfer.md)             | <span data-ttu-id="9ae81-124">**Item** 物件的 [**Transfer**](-wia-iwiadispatchitem-transfer.md)方法會將資料從裝置傳送到檔案。</span><span class="sxs-lookup"><span data-stu-id="9ae81-124">The [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of the **Item** object transfers data from a device to a file.</span></span> <span data-ttu-id="9ae81-125">此方法僅適用于裝置類型專案。</span><span class="sxs-lookup"><span data-stu-id="9ae81-125">This method applies only to device type items.</span></span><br/>                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="9ae81-126">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae81-126">Properties</span></span>

<span data-ttu-id="9ae81-127">**Item** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae81-127">The **Item** object has these properties.</span></span>



| <span data-ttu-id="9ae81-128">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae81-128">Property</span></span>                                                                    | <span data-ttu-id="9ae81-129">存取類型</span><span class="sxs-lookup"><span data-stu-id="9ae81-129">Access type</span></span>          | <span data-ttu-id="9ae81-130">Description</span><span class="sxs-lookup"><span data-stu-id="9ae81-130">Description</span></span>                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ae81-131">**Children**</span><span class="sxs-lookup"><span data-stu-id="9ae81-131">**Children**</span></span>](-wia-iwiadispatchitem-children.md)<br/>               | <span data-ttu-id="9ae81-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-132">Read-only</span></span><br/> | <span data-ttu-id="9ae81-133">**Item** 物件的 [**子**](-wia-iwiadispatchitem-children.md)屬性會抓取 **專案** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="9ae81-133">The [**Children**](-wia-iwiadispatchitem-children.md) property of the **Item** object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="9ae81-134">這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。</span><span class="sxs-lookup"><span data-stu-id="9ae81-134">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <br/> |
| [<span data-ttu-id="9ae81-135">**ConnectStatus**</span><span class="sxs-lookup"><span data-stu-id="9ae81-135">**ConnectStatus**</span></span>](-wia-iwiadispatchitem-connectstatus.md)<br/>     | <span data-ttu-id="9ae81-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-136">Read-only</span></span><br/> | <span data-ttu-id="9ae81-137">抓取裝置的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="9ae81-137">Retrieves the connection status of the device.</span></span> <span data-ttu-id="9ae81-138">這個屬性只適用于) 的裝置 (根專案類型專案。</span><span class="sxs-lookup"><span data-stu-id="9ae81-138">This property applies only to items of type device (root items).</span></span> <span data-ttu-id="9ae81-139">如果這個屬性不會套用至專案) ，可能的值為「已連線」、「已中斷連線」或 **Null** (。</span><span class="sxs-lookup"><span data-stu-id="9ae81-139">Possible values are "connected", "disconnected", or **NULL** (if this property does not apply to the item).</span></span> <br/>                     |
| [<span data-ttu-id="9ae81-140">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="9ae81-140">**FirmwareVersion**</span></span>](-wia-iwiadispatchitem-firmwareversion.md)<br/> | <span data-ttu-id="9ae81-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-141">Read-only</span></span><br/> | <span data-ttu-id="9ae81-142">捕獲裝置的固件版本。</span><span class="sxs-lookup"><span data-stu-id="9ae81-142">Retrieves the firmware version of the device.</span></span> <span data-ttu-id="9ae81-143">這個屬性只適用于) 的裝置 (根專案類型專案。</span><span class="sxs-lookup"><span data-stu-id="9ae81-143">This property applies only to items of type device (root items).</span></span> <br/>                                                                                                                                  |
| [<span data-ttu-id="9ae81-144">**FullName**</span><span class="sxs-lookup"><span data-stu-id="9ae81-144">**FullName**</span></span>](-wia-iwiadispatchitem-fullname.md)<br/>               | <span data-ttu-id="9ae81-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-145">Read-only</span></span><br/> | <span data-ttu-id="9ae81-146">抓取專案顯示在 UI 中的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae81-146">Retrieves the full name of the item as it appears in the UI.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="9ae81-147">**高度**</span><span class="sxs-lookup"><span data-stu-id="9ae81-147">**Height**</span></span>](-wia-iwiadispatchitem-height.md)<br/>                   | <span data-ttu-id="9ae81-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-148">Read-only</span></span><br/> | <span data-ttu-id="9ae81-149">專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-149">The height, in pixels, of the item.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="9ae81-150">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="9ae81-150">**ItemType**</span></span>](-wia-iwiadispatchitem-itemtype.md)<br/>               | <span data-ttu-id="9ae81-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-151">Read-only</span></span><br/> | <span data-ttu-id="9ae81-152">這個專案的型別。</span><span class="sxs-lookup"><span data-stu-id="9ae81-152">The type of this item.</span></span> <br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="9ae81-153">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ae81-153">**Name**</span></span>](-wia-iwiadispatchitem-name.md)<br/>                       | <span data-ttu-id="9ae81-154">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-154">Read-only</span></span><br/> | <span data-ttu-id="9ae81-155">顯示在 UI 中的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae81-155">The name of the item as it appears in the UI.</span></span> <br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="9ae81-156">**PictureHeight**</span><span class="sxs-lookup"><span data-stu-id="9ae81-156">**PictureHeight**</span></span>](-wia-iwiadispatchitem-pictureheight.md)<br/>     | <span data-ttu-id="9ae81-157">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-157">Read-only</span></span><br/> | <span data-ttu-id="9ae81-158">此數位相機所產生影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-158">The height, in pixels, of images produced by this digital camera.</span></span> <span data-ttu-id="9ae81-159">僅適用于數位相機。</span><span class="sxs-lookup"><span data-stu-id="9ae81-159">Applies only to digital cameras.</span></span> <br/>                                                                                                                                              |
| [<span data-ttu-id="9ae81-160">**PictureWidth**</span><span class="sxs-lookup"><span data-stu-id="9ae81-160">**PictureWidth**</span></span>](-wia-iwiadispatchitem-picturewidth.md)<br/>       | <span data-ttu-id="9ae81-161">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-161">Read-only</span></span><br/> | <span data-ttu-id="9ae81-162">此數位相機所產生影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-162">The width, in pixels, of images produced by this digital camera.</span></span> <span data-ttu-id="9ae81-163">僅適用于數位相機。</span><span class="sxs-lookup"><span data-stu-id="9ae81-163">Applies only to digital cameras.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="9ae81-164">**ThumbHeight**</span><span class="sxs-lookup"><span data-stu-id="9ae81-164">**ThumbHeight**</span></span>](-wia-iwiadispatchitem-thumbheight.md)<br/>         | <span data-ttu-id="9ae81-165">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-165">Read-only</span></span><br/> | <span data-ttu-id="9ae81-166">縮圖影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-166">The height, in pixels, of the thumbnail image.</span></span> <span data-ttu-id="9ae81-167">如果這個專案不支援縮圖，這個屬性會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="9ae81-167">This property returns -1 if this item does not support thumbnails.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="9ae81-168">**縮圖**</span><span class="sxs-lookup"><span data-stu-id="9ae81-168">**Thumbnail**</span></span>](-wia-iwiadispatchitem-thumbnail.md)<br/>             | <span data-ttu-id="9ae81-169">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-169">Read-only</span></span><br/> | <span data-ttu-id="9ae81-170">縮圖影像的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="9ae81-170">The path and filename of the thumbnail image.</span></span> <span data-ttu-id="9ae81-171">如果專案不支援縮圖，或如果無法建立路徑，則此屬性為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9ae81-171">This property is **NULL** if the item does not support thumbnails, or if a path cannot be built.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="9ae81-172">**ThumbWidth**</span><span class="sxs-lookup"><span data-stu-id="9ae81-172">**ThumbWidth**</span></span>](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | <span data-ttu-id="9ae81-173">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-173">Read-only</span></span><br/> | <span data-ttu-id="9ae81-174">縮圖影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-174">The width, in pixels, of the thumbnail image.</span></span> <span data-ttu-id="9ae81-175">如果這個專案不支援縮圖，這個屬性會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="9ae81-175">This property returns -1 if this item does not support thumbnails.</span></span> <br/>                                                                                                                                |
| [<span data-ttu-id="9ae81-176">**時間**</span><span class="sxs-lookup"><span data-stu-id="9ae81-176">**Time**</span></span>](-wia-iwiadispatchitem-time.md)<br/>                       | <span data-ttu-id="9ae81-177">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-177">Read-only</span></span><br/> | <span data-ttu-id="9ae81-178">目前的時間。</span><span class="sxs-lookup"><span data-stu-id="9ae81-178">The current time.</span></span> <span data-ttu-id="9ae81-179">僅適用于裝置。</span><span class="sxs-lookup"><span data-stu-id="9ae81-179">Applies only to devices.</span></span> <br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="9ae81-180">**寬度**</span><span class="sxs-lookup"><span data-stu-id="9ae81-180">**Width**</span></span>](-wia-iwiadispatchitem-width.md)<br/>                     | <span data-ttu-id="9ae81-181">唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae81-181">Read-only</span></span><br/> | <span data-ttu-id="9ae81-182">專案的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae81-182">The width, in pixels, of the item.</span></span> <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="9ae81-183">備註</span><span class="sxs-lookup"><span data-stu-id="9ae81-183">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="9ae81-184">建立 \\ 存取函數</span><span class="sxs-lookup"><span data-stu-id="9ae81-184">Creation\\Access Functions</span></span>

<span data-ttu-id="9ae81-185">使用下列任何一項來取得物件的參考：</span><span class="sxs-lookup"><span data-stu-id="9ae81-185">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="9ae81-186">**TakePicture**</span><span class="sxs-lookup"><span data-stu-id="9ae81-186">**TakePicture**</span></span>](-wia-iwiadispatchitem-takepicture.md)

[<span data-ttu-id="9ae81-187">**建立**</span><span class="sxs-lookup"><span data-stu-id="9ae81-187">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)

[<span data-ttu-id="9ae81-188">**建立**</span><span class="sxs-lookup"><span data-stu-id="9ae81-188">**Create**</span></span>](-wia-iwia-create.md)



 

## <a name="requirements"></a><span data-ttu-id="9ae81-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ae81-189">Requirements</span></span>



| <span data-ttu-id="9ae81-190">需求</span><span class="sxs-lookup"><span data-stu-id="9ae81-190">Requirement</span></span> | <span data-ttu-id="9ae81-191">值</span><span class="sxs-lookup"><span data-stu-id="9ae81-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae81-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ae81-192">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae81-193">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ae81-193">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ae81-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ae81-194">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae81-195">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ae81-195">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9ae81-196">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae81-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae81-197"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9ae81-197"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




