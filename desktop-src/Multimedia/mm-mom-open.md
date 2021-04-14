---
title: 'MM_MOM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 當開啟 MIDI 輸出裝置時，會將 [MOM OPEN] 訊息傳送至視窗。'
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464216"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="59014-104">MM \_ MOM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="59014-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="59014-105">當開啟 MIDI 輸出裝置時，會將 [ **\_ MOM \_ OPEN** ] 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="59014-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="59014-106">參數</span><span class="sxs-lookup"><span data-stu-id="59014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59014-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="59014-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="59014-108">MIDI 輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="59014-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="59014-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="59014-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="59014-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="59014-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59014-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="59014-111">Return Value</span></span>

<span data-ttu-id="59014-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="59014-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59014-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="59014-113">Requirements</span></span>



| <span data-ttu-id="59014-114">需求</span><span class="sxs-lookup"><span data-stu-id="59014-114">Requirement</span></span> | <span data-ttu-id="59014-115">值</span><span class="sxs-lookup"><span data-stu-id="59014-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59014-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59014-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59014-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59014-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59014-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59014-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59014-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59014-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59014-120">標頭</span><span class="sxs-lookup"><span data-stu-id="59014-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59014-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="59014-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59014-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59014-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59014-123">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="59014-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





