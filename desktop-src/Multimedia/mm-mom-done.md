---
title: 'MM_MOM_DONE 訊息 (Mmsystem .h) '
description: '\_ \_ 當已播放指定的 MIDI 系統專屬或串流緩衝區，並將其傳回給應用程式時，就會將 MM MOM 完成訊息傳送至視窗。'
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024700"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="866e9-104">MM \_ MOM \_ 完成訊息</span><span class="sxs-lookup"><span data-stu-id="866e9-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="866e9-105">當已播放指定的 MIDI 系統專屬或串流緩衝區，並將其傳回給應用程式時，就會將 **MM \_ MOM \_ 完成** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="866e9-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="866e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="866e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866e9-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="866e9-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="866e9-108">播放緩衝區之 MIDI 輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="866e9-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="866e9-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="866e9-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="866e9-110">識別緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="866e9-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866e9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="866e9-111">Return Value</span></span>

<span data-ttu-id="866e9-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="866e9-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="866e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="866e9-113">Requirements</span></span>



| <span data-ttu-id="866e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="866e9-114">Requirement</span></span> | <span data-ttu-id="866e9-115">值</span><span class="sxs-lookup"><span data-stu-id="866e9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="866e9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="866e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="866e9-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="866e9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="866e9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="866e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="866e9-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="866e9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="866e9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="866e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="866e9-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="866e9-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="866e9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="866e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866e9-123">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="866e9-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

