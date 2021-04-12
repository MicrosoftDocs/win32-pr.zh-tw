---
title: 'MOM_DONE 訊息 (Mciapi .h) '
description: '\_當已播放指定的系統專屬或資料流程緩衝區，並將其傳回給應用程式時，MOM 完成的訊息會傳送至 MIDI 輸出回呼函式。'
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE message Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384394"
---
# <a name="mom_done-message"></a><span data-ttu-id="9bffa-104">MOM \_ 完成訊息</span><span class="sxs-lookup"><span data-stu-id="9bffa-104">MOM\_DONE message</span></span>

<span data-ttu-id="9bffa-105">當已播放指定的系統專屬或資料流程緩衝區，並將其傳回給應用程式時， **MOM \_ 完成** 的訊息會傳送至 MIDI 輸出回呼函式。</span><span class="sxs-lookup"><span data-stu-id="9bffa-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9bffa-106">參數</span><span class="sxs-lookup"><span data-stu-id="9bffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bffa-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="9bffa-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="9bffa-108">識別緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9bffa-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9bffa-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9bffa-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9bffa-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="9bffa-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bffa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bffa-111">Return Value</span></span>

<span data-ttu-id="9bffa-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9bffa-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bffa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bffa-113">Requirements</span></span>



| <span data-ttu-id="9bffa-114">需求</span><span class="sxs-lookup"><span data-stu-id="9bffa-114">Requirement</span></span> | <span data-ttu-id="9bffa-115">值</span><span class="sxs-lookup"><span data-stu-id="9bffa-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bffa-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bffa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9bffa-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bffa-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9bffa-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bffa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9bffa-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bffa-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9bffa-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9bffa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bffa-121"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bffa-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bffa-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bffa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bffa-123">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="9bffa-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

