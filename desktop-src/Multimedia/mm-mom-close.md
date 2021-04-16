---
title: 'MM_MOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當 MIDI 輸出裝置關閉時，會將 MM MOM 關閉訊息傳送至視窗。'
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464497"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="b34b2-104">MM \_ MOM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="b34b2-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="b34b2-105">當 MIDI 輸出裝置關閉時，會將 **MM \_ MOM \_ 關閉** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="b34b2-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b34b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="b34b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34b2-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="b34b2-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="b34b2-108">MIDI 輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b34b2-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="b34b2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b34b2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b34b2-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b34b2-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34b2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b34b2-111">Return Value</span></span>

<span data-ttu-id="b34b2-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b34b2-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34b2-113">備註</span><span class="sxs-lookup"><span data-stu-id="b34b2-113">Remarks</span></span>

<span data-ttu-id="b34b2-114">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="b34b2-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34b2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b34b2-115">Requirements</span></span>



| <span data-ttu-id="b34b2-116">需求</span><span class="sxs-lookup"><span data-stu-id="b34b2-116">Requirement</span></span> | <span data-ttu-id="b34b2-117">值</span><span class="sxs-lookup"><span data-stu-id="b34b2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34b2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b34b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b34b2-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b34b2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b34b2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b34b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b34b2-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b34b2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b34b2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b34b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34b2-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b34b2-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34b2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b34b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34b2-125">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="b34b2-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





