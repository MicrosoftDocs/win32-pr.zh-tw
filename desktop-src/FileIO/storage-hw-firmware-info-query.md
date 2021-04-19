---
description: 此結構包含裝置固件的相關資訊。
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: 'STORAGE_HW_FIRMWARE_INFO_QUERY 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981577"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="0af4c-103">儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢結構</span><span class="sxs-lookup"><span data-stu-id="0af4c-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="0af4c-104">此結構包含裝置固件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0af4c-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af4c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0af4c-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="0af4c-106">成員</span><span class="sxs-lookup"><span data-stu-id="0af4c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0af4c-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="0af4c-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0af4c-108">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="0af4c-108">The version of this structure.</span></span> <span data-ttu-id="0af4c-109">這應該設定為 sizeof (儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢) </span><span class="sxs-lookup"><span data-stu-id="0af4c-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="0af4c-110">**大小**</span><span class="sxs-lookup"><span data-stu-id="0af4c-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="0af4c-111">此結構的大小，表示為緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0af4c-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0af4c-112">**旗標**</span><span class="sxs-lookup"><span data-stu-id="0af4c-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0af4c-113">與查詢相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="0af4c-113">The flags associated with the query.</span></span> <span data-ttu-id="0af4c-114">以下是可以在這個成員中設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="0af4c-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="0af4c-115">旗標</span><span class="sxs-lookup"><span data-stu-id="0af4c-115">Flag</span></span>                                             | <span data-ttu-id="0af4c-116">描述</span><span class="sxs-lookup"><span data-stu-id="0af4c-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0af4c-117">儲存體 \_ HW \_ 固件 \_ 要求 \_ 旗標 \_ 控制器</span><span class="sxs-lookup"><span data-stu-id="0af4c-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="0af4c-118">指出裝置手動/物件本身以外的要求目標。</span><span class="sxs-lookup"><span data-stu-id="0af4c-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0af4c-119">**已保留**</span><span class="sxs-lookup"><span data-stu-id="0af4c-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0af4c-120">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="0af4c-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0af4c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0af4c-121">Requirements</span></span>



| <span data-ttu-id="0af4c-122">需求</span><span class="sxs-lookup"><span data-stu-id="0af4c-122">Requirement</span></span> | <span data-ttu-id="0af4c-123">值</span><span class="sxs-lookup"><span data-stu-id="0af4c-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af4c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0af4c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0af4c-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af4c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="0af4c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0af4c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0af4c-127">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0af4c-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="0af4c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0af4c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af4c-129"><dt>Winioctl (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0af4c-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af4c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0af4c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af4c-131">**\_啟用 IOCTL 儲存體 \_ 固件 \_**</span><span class="sxs-lookup"><span data-stu-id="0af4c-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="0af4c-132">**儲存體 \_ HW \_ 固件 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="0af4c-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="0af4c-133">**IOCTL \_ 儲存體 \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="0af4c-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="0af4c-134">**儲存體 \_ HW \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="0af4c-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="0af4c-135">**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0af4c-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="0af4c-136">**儲存體 \_ HW \_ 固件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0af4c-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="0af4c-137">**儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0af4c-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




