---
description: STORAGE_HW_FIRMWARE_INFO 結構-此結構包含裝置固件的相關資訊。
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: 'STORAGE_HW_FIRMWARE_INFO 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090956"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="db19b-103">儲存體 \_ HW \_ 固件 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="db19b-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="db19b-104">此結構包含裝置固件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="db19b-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="db19b-105">語法</span><span class="sxs-lookup"><span data-stu-id="db19b-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="db19b-106">成員</span><span class="sxs-lookup"><span data-stu-id="db19b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="db19b-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="db19b-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-108">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="db19b-108">The version of this structure.</span></span> <span data-ttu-id="db19b-109">這應該設定為 sizeof (儲存體 \_ HW \_ 固件 \_ 資訊) </span><span class="sxs-lookup"><span data-stu-id="db19b-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="db19b-110">**大小**</span><span class="sxs-lookup"><span data-stu-id="db19b-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-111">此結構的大小，表示為包含位置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db19b-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="db19b-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-113">指出此固件支援升級。</span><span class="sxs-lookup"><span data-stu-id="db19b-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="db19b-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-115">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="db19b-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="db19b-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-117">裝置上的固件插槽數目。</span><span class="sxs-lookup"><span data-stu-id="db19b-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="db19b-118">這是插槽陣列的維度。</span><span class="sxs-lookup"><span data-stu-id="db19b-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="db19b-119">某些裝置可以儲存1個以上的固件映射（如果有一個以上的固件插槽）。</span><span class="sxs-lookup"><span data-stu-id="db19b-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="db19b-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="db19b-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-121">包含目前作用中/正在執行之固件映射的固件位置。</span><span class="sxs-lookup"><span data-stu-id="db19b-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="db19b-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-123">暫止啟用的固件插槽。</span><span class="sxs-lookup"><span data-stu-id="db19b-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="db19b-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-125">指出此固件同時適用于裝置和控制器/介面卡，例如 NVMe SSD。</span><span class="sxs-lookup"><span data-stu-id="db19b-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-126">**已保留**</span><span class="sxs-lookup"><span data-stu-id="db19b-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-127">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="db19b-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="db19b-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-129">影像承載的對齊（以位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="db19b-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="db19b-130">最大值為頁面 \_ 大小。</span><span class="sxs-lookup"><span data-stu-id="db19b-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="db19b-131">傳輸大小是此大小的其中一種。</span><span class="sxs-lookup"><span data-stu-id="db19b-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="db19b-132">某些通訊協定需要的磁區大小至少為磁區。</span><span class="sxs-lookup"><span data-stu-id="db19b-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="db19b-133">當此值設定為0時，表示此值無效。</span><span class="sxs-lookup"><span data-stu-id="db19b-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="db19b-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-135">映射裝載大小上限，這會用於單一命令。</span><span class="sxs-lookup"><span data-stu-id="db19b-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="db19b-136">**位置**</span><span class="sxs-lookup"><span data-stu-id="db19b-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="db19b-137">包含裝置上每個插槽的位置資訊，其類型為 [**儲存體 \_ HW \_ 固件 \_ 位置 \_ 資訊**](storage-hw-firmware-slot-info.md)。</span><span class="sxs-lookup"><span data-stu-id="db19b-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db19b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="db19b-138">Requirements</span></span>



| <span data-ttu-id="db19b-139">需求</span><span class="sxs-lookup"><span data-stu-id="db19b-139">Requirement</span></span> | <span data-ttu-id="db19b-140">值</span><span class="sxs-lookup"><span data-stu-id="db19b-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db19b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db19b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="db19b-142">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db19b-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="db19b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db19b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="db19b-144">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db19b-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="db19b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="db19b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="db19b-146"><dt>Winioctl (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="db19b-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db19b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db19b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db19b-148">**\_啟用 IOCTL 儲存體 \_ 固件 \_**</span><span class="sxs-lookup"><span data-stu-id="db19b-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="db19b-149">**儲存體 \_ HW \_ 固件 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="db19b-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="db19b-150">**IOCTL \_ 儲存體 \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="db19b-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="db19b-151">**儲存體 \_ HW \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="db19b-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="db19b-152">**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="db19b-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="db19b-153">**儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="db19b-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="db19b-154">**儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="db19b-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




