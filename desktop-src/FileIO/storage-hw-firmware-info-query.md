---
description: STORAGE_HW_FIRMWARE_INFO_QUERY 結構-此結構包含裝置固件的相關資訊。
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
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119396"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="b2a8f-103">儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢結構</span><span class="sxs-lookup"><span data-stu-id="b2a8f-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="b2a8f-104">此結構包含裝置固件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2a8f-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="b2a8f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b2a8f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2a8f-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="b2a8f-108">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-108">The version of this structure.</span></span> <span data-ttu-id="b2a8f-109">這應該設定為 sizeof (儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢) </span><span class="sxs-lookup"><span data-stu-id="b2a8f-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="b2a8f-110">**大小**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b2a8f-111">此結構的大小，表示為緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b2a8f-112">**旗標**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b2a8f-113">與查詢相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-113">The flags associated with the query.</span></span> <span data-ttu-id="b2a8f-114">以下是可以在這個成員中設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="b2a8f-115">旗標</span><span class="sxs-lookup"><span data-stu-id="b2a8f-115">Flag</span></span>                                             | <span data-ttu-id="b2a8f-116">描述</span><span class="sxs-lookup"><span data-stu-id="b2a8f-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a8f-117">儲存體 \_ HW \_ 固件 \_ 要求 \_ 旗標 \_ 控制器</span><span class="sxs-lookup"><span data-stu-id="b2a8f-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="b2a8f-118">指出裝置手動/物件本身以外的要求目標。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b2a8f-119">**已保留**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b2a8f-120">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b2a8f-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2a8f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2a8f-121">Requirements</span></span>



| <span data-ttu-id="b2a8f-122">需求</span><span class="sxs-lookup"><span data-stu-id="b2a8f-122">Requirement</span></span> | <span data-ttu-id="b2a8f-123">值</span><span class="sxs-lookup"><span data-stu-id="b2a8f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a8f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2a8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a8f-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2a8f-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="b2a8f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2a8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a8f-127">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2a8f-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b2a8f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b2a8f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2a8f-129"><dt>Winioctl (包含 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b2a8f-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2a8f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2a8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a8f-131">**\_啟用 IOCTL 儲存體 \_ 固件 \_**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="b2a8f-132">**儲存體 \_ HW \_ 固件 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="b2a8f-133">**IOCTL \_ 儲存體 \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="b2a8f-134">**儲存體 \_ HW \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="b2a8f-135">**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="b2a8f-136">**儲存體 \_ HW \_ 固件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="b2a8f-137">**儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b2a8f-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




