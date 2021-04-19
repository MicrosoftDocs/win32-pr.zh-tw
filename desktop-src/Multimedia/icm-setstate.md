---
title: 'ICM_SETSTATE 訊息 (Vfw .h) '
description: ICM \_ SETSTATE 訊息會通知視訊壓縮驅動程式，以設定壓縮程式的狀態。 您可以使用 ICSetState 宏明確地傳送此訊息。
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965954"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="44d68-105">ICM \_ SETSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="44d68-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="44d68-106">**ICM \_ SETSTATE** 訊息會通知視訊壓縮驅動程式，以設定壓縮程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="44d68-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="44d68-107">您可以使用 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="44d68-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="44d68-108">參數</span><span class="sxs-lookup"><span data-stu-id="44d68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d68-109"><span id="pv"></span><span id="PV"></span>*光伏*</span><span class="sxs-lookup"><span data-stu-id="44d68-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="44d68-110">包含設定資料之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="44d68-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="44d68-111">您可以為此參數指定 **Null** ，以將壓縮程式重設為預設狀態。</span><span class="sxs-lookup"><span data-stu-id="44d68-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="44d68-112"><span id="cb"></span><span id="CB"></span>*Cb*</span><span class="sxs-lookup"><span data-stu-id="44d68-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="44d68-113">記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="44d68-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d68-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="44d68-114">Return Value</span></span>

<span data-ttu-id="44d68-115">如果成功，則傳回壓縮程式所使用的位元組數目，否則為零。</span><span class="sxs-lookup"><span data-stu-id="44d68-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d68-116">備註</span><span class="sxs-lookup"><span data-stu-id="44d68-116">Remarks</span></span>

<span data-ttu-id="44d68-117">這則訊息所使用的資訊是私用的，而且是指定之壓縮程式的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="44d68-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="44d68-118">用戶端應用程式應該只使用此訊息來還原先前以 [**ICM \_ >getstate**](icm-getstate.md) 訊息取得的資訊，而且應該使用 ICM 設定訊息來調整視訊壓縮驅動程式的 [**\_ 設定**](icm-configure.md) 。</span><span class="sxs-lookup"><span data-stu-id="44d68-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d68-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d68-119">Requirements</span></span>



| <span data-ttu-id="44d68-120">需求</span><span class="sxs-lookup"><span data-stu-id="44d68-120">Requirement</span></span> | <span data-ttu-id="44d68-121">值</span><span class="sxs-lookup"><span data-stu-id="44d68-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="44d68-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44d68-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44d68-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d68-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="44d68-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44d68-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44d68-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d68-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44d68-126">標頭</span><span class="sxs-lookup"><span data-stu-id="44d68-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d68-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="44d68-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d68-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44d68-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d68-129">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="44d68-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="44d68-130">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="44d68-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





