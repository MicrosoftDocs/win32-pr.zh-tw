---
title: 'MOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_當 midi 輸出裝置關閉時，MOM 關閉訊息會傳送至 midi 輸出回呼函式。'
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934994"
---
# <a name="mom_close-message"></a><span data-ttu-id="aecd9-104">MOM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="aecd9-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="aecd9-105">當 MIDI 輸出裝置關閉時， **MOM \_ 關閉** 訊息會傳送至 midi 輸出回呼函式。</span><span class="sxs-lookup"><span data-stu-id="aecd9-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="aecd9-106">參數</span><span class="sxs-lookup"><span data-stu-id="aecd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aecd9-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="aecd9-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="aecd9-108">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="aecd9-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="aecd9-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="aecd9-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="aecd9-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="aecd9-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aecd9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aecd9-111">Return Value</span></span>

<span data-ttu-id="aecd9-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aecd9-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aecd9-113">備註</span><span class="sxs-lookup"><span data-stu-id="aecd9-113">Remarks</span></span>

<span data-ttu-id="aecd9-114">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="aecd9-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecd9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aecd9-115">Requirements</span></span>



| <span data-ttu-id="aecd9-116">需求</span><span class="sxs-lookup"><span data-stu-id="aecd9-116">Requirement</span></span> | <span data-ttu-id="aecd9-117">值</span><span class="sxs-lookup"><span data-stu-id="aecd9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecd9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aecd9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aecd9-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aecd9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aecd9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aecd9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aecd9-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aecd9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aecd9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aecd9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aecd9-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aecd9-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecd9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aecd9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecd9-125">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="aecd9-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





