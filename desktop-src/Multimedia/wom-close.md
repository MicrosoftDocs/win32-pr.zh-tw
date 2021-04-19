---
title: 'WOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_當波形音訊輸出裝置關閉時，WOM 關閉訊息會傳送至波形音訊輸出回呼函式。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996576"
---
# <a name="wom_close-message"></a><span data-ttu-id="9a855-105">WOM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="9a855-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="9a855-106">當波形音訊輸出裝置關閉時， **WOM \_ 關閉** 訊息會傳送至波形音訊輸出回呼函式。</span><span class="sxs-lookup"><span data-stu-id="9a855-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="9a855-107">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="9a855-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9a855-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a855-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9a855-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9a855-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="9a855-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a855-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9a855-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9a855-112">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="9a855-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a855-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a855-113">Return Value</span></span>

<span data-ttu-id="9a855-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9a855-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a855-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a855-115">Requirements</span></span>



| <span data-ttu-id="9a855-116">需求</span><span class="sxs-lookup"><span data-stu-id="9a855-116">Requirement</span></span> | <span data-ttu-id="9a855-117">值</span><span class="sxs-lookup"><span data-stu-id="9a855-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a855-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a855-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a855-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a855-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a855-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a855-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a855-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a855-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a855-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9a855-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a855-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9a855-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a855-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a855-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a855-125">波形音訊</span><span class="sxs-lookup"><span data-stu-id="9a855-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="9a855-126">波形訊息</span><span class="sxs-lookup"><span data-stu-id="9a855-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





