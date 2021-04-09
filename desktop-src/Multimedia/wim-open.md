---
title: 'WIM_OPEN 訊息 (Mmsystem .h) '
description: '\_開啟波形音訊輸入裝置時，會將 WIM 開啟的訊息傳送到波形音訊輸入回撥函式。'
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- WIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934933"
---
# <a name="wim_open-message"></a><span data-ttu-id="c8081-104">WIM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="c8081-104">WIM\_OPEN message</span></span>

<span data-ttu-id="c8081-105">開啟波形音訊輸入裝置時，會將 **WIM \_ 開啟** 的訊息傳送到波形音訊輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="c8081-105">The **WIM\_OPEN** message is sent to a waveform-audio input callback function when a waveform-audio input device is opened.</span></span>


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="c8081-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8081-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8081-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c8081-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c8081-108">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="c8081-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8081-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c8081-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c8081-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="c8081-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8081-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8081-111">Return Value</span></span>

<span data-ttu-id="c8081-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8081-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8081-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8081-113">Requirements</span></span>



| <span data-ttu-id="c8081-114">需求</span><span class="sxs-lookup"><span data-stu-id="c8081-114">Requirement</span></span> | <span data-ttu-id="c8081-115">值</span><span class="sxs-lookup"><span data-stu-id="c8081-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8081-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8081-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8081-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8081-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8081-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8081-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8081-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8081-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8081-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c8081-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8081-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c8081-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8081-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8081-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8081-123">波形音訊</span><span class="sxs-lookup"><span data-stu-id="c8081-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="c8081-124">波形訊息</span><span class="sxs-lookup"><span data-stu-id="c8081-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





