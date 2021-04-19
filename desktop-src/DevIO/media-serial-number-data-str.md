---
description: 包含 USB 裝置的序號。 它是由 IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號控制項程式 \_ 代碼所使用。
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997314"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="73713-104">媒體 \_ 序號 \_ \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="73713-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="73713-105">包含 USB 裝置的序號。</span><span class="sxs-lookup"><span data-stu-id="73713-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="73713-106">它是由 [**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號 \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) 控制項程式碼所使用。</span><span class="sxs-lookup"><span data-stu-id="73713-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="73713-107">語法</span><span class="sxs-lookup"><span data-stu-id="73713-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="73713-108">成員</span><span class="sxs-lookup"><span data-stu-id="73713-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="73713-109">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="73713-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="73713-110">**SerialNumberData** 字串的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="73713-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="73713-111">**結果**</span><span class="sxs-lookup"><span data-stu-id="73713-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="73713-112">要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="73713-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="73713-113">**已保留**</span><span class="sxs-lookup"><span data-stu-id="73713-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="73713-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="73713-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="73713-115">**SerialNumberData**</span><span class="sxs-lookup"><span data-stu-id="73713-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="73713-116">裝置的序號。</span><span class="sxs-lookup"><span data-stu-id="73713-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73713-117">備註</span><span class="sxs-lookup"><span data-stu-id="73713-117">Remarks</span></span>

<span data-ttu-id="73713-118">**媒體 \_ 序號 \_ \_ 資料** 結構沒有可用的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="73713-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="73713-119">在您的原始程式碼中，將結構定義包含在此頁面的頂端。</span><span class="sxs-lookup"><span data-stu-id="73713-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73713-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="73713-120">Requirements</span></span>



| <span data-ttu-id="73713-121">需求</span><span class="sxs-lookup"><span data-stu-id="73713-121">Requirement</span></span> | <span data-ttu-id="73713-122">值</span><span class="sxs-lookup"><span data-stu-id="73713-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="73713-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73713-123">Minimum supported client</span></span><br/> | <span data-ttu-id="73713-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="73713-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="73713-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73713-125">Minimum supported server</span></span><br/> | <span data-ttu-id="73713-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73713-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73713-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73713-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73713-128">**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號 \_**</span><span class="sxs-lookup"><span data-stu-id="73713-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




