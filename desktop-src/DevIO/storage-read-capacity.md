---
description: 包含裝置大小的相關資訊。 這會從 IOCTL \_ 儲存體 \_ 讀取 \_ 容量控制程式代碼傳回。
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: 'STORAGE_READ_CAPACITY 結構 (Ntddstor .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385890"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="a9ac1-104">儲存體 \_ 讀取 \_ 容量結構</span><span class="sxs-lookup"><span data-stu-id="a9ac1-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="a9ac1-105">包含裝置大小的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-105">Contains information about the size of a device.</span></span> <span data-ttu-id="a9ac1-106">這會從 [**IOCTL \_ 儲存體 \_ 讀取 \_ 容量**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) 控制程式代碼傳回。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ac1-107">語法</span><span class="sxs-lookup"><span data-stu-id="a9ac1-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="a9ac1-108">成員</span><span class="sxs-lookup"><span data-stu-id="a9ac1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9ac1-109">**版本**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-110">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-110">The version of this structure.</span></span> <span data-ttu-id="a9ac1-111">呼叫端必須將這個成員設定為 `sizeof(STORAGE_READ_CAPACITY)` 。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="a9ac1-112">**大小**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-113">傳回的資料大小。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="a9ac1-114">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-115">每個區塊的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="a9ac1-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-117">磁片上的區塊總數。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="a9ac1-118">**DiskLength**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-119">磁片大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9ac1-120">備註</span><span class="sxs-lookup"><span data-stu-id="a9ac1-120">Remarks</span></span>

<span data-ttu-id="a9ac1-121">標頭檔 Ntddstor 可在 Windows 驅動程式套件 (WDK) 中取得。</span><span class="sxs-lookup"><span data-stu-id="a9ac1-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ac1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9ac1-122">Requirements</span></span>



| <span data-ttu-id="a9ac1-123">需求</span><span class="sxs-lookup"><span data-stu-id="a9ac1-123">Requirement</span></span> | <span data-ttu-id="a9ac1-124">值</span><span class="sxs-lookup"><span data-stu-id="a9ac1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ac1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9ac1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ac1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9ac1-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a9ac1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9ac1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ac1-128">Windows Server 2008、Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="a9ac1-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="a9ac1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a9ac1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ac1-130"><dt>Ntddstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ac1-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ac1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9ac1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ac1-132">**IOCTL \_ 儲存體 \_ 讀取 \_ 容量**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




