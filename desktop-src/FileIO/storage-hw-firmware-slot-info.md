---
description: 此結構包含裝置上某個位置的相關資訊。
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: 'STORAGE_HW_FIRMWARE_SLOT_INFO 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001343"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="3ec65-103">儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="3ec65-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="3ec65-104">此結構包含裝置上某個位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ec65-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec65-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ec65-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="3ec65-106">成員</span><span class="sxs-lookup"><span data-stu-id="3ec65-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ec65-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="3ec65-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-108">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="3ec65-108">The version of this structure.</span></span> <span data-ttu-id="3ec65-109">這應該設定為 sizeof (儲存體 \_ HW \_ 固件插槽 \_ 的 \_ 資訊) </span><span class="sxs-lookup"><span data-stu-id="3ec65-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-110">**大小**</span><span class="sxs-lookup"><span data-stu-id="3ec65-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-111">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="3ec65-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="3ec65-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-113">此位置的插槽號碼。</span><span class="sxs-lookup"><span data-stu-id="3ec65-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-114">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="3ec65-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-115">指出此位置是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="3ec65-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="3ec65-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-117">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="3ec65-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="3ec65-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="3ec65-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3ec65-120">**修訂**</span><span class="sxs-lookup"><span data-stu-id="3ec65-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="3ec65-121">此位置上的固件修訂。</span><span class="sxs-lookup"><span data-stu-id="3ec65-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ec65-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec65-122">Requirements</span></span>



| <span data-ttu-id="3ec65-123">需求</span><span class="sxs-lookup"><span data-stu-id="3ec65-123">Requirement</span></span> | <span data-ttu-id="3ec65-124">值</span><span class="sxs-lookup"><span data-stu-id="3ec65-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec65-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec65-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec65-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec65-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="3ec65-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec65-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec65-128">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec65-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="3ec65-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3ec65-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec65-130"><dt>Winioctl (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3ec65-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec65-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec65-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec65-132">**\_啟用 IOCTL 儲存體 \_ 固件 \_**</span><span class="sxs-lookup"><span data-stu-id="3ec65-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="3ec65-133">**儲存體 \_ HW \_ 固件 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="3ec65-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="3ec65-134">**IOCTL \_ 儲存體 \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="3ec65-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="3ec65-135">**儲存體 \_ HW \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="3ec65-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="3ec65-136">**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3ec65-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="3ec65-137">**儲存體 \_ HW \_ 固件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3ec65-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="3ec65-138">**儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="3ec65-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




