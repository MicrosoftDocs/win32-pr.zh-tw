---
title: 'WOM_OPEN 訊息 (Mmsystem .h) '
description: '\_開啟波形音訊輸出裝置時，WOM 開啟的訊息會傳送到波形音訊輸出回呼函式。'
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093784"
---
# <a name="wom_open-message"></a><span data-ttu-id="fa1e3-104">WOM \_ 開啟的訊息</span><span class="sxs-lookup"><span data-stu-id="fa1e3-104">WOM\_OPEN message</span></span>

<span data-ttu-id="fa1e3-105">開啟波形音訊輸出裝置時， **WOM \_ 開啟** 的訊息會傳送到波形音訊輸出回呼函式。</span><span class="sxs-lookup"><span data-stu-id="fa1e3-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="fa1e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa1e3-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fa1e3-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fa1e3-108">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="fa1e3-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fa1e3-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fa1e3-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fa1e3-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="fa1e3-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa1e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa1e3-111">Return Value</span></span>

<span data-ttu-id="fa1e3-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa1e3-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1e3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa1e3-113">Requirements</span></span>



| <span data-ttu-id="fa1e3-114">需求</span><span class="sxs-lookup"><span data-stu-id="fa1e3-114">Requirement</span></span> | <span data-ttu-id="fa1e3-115">值</span><span class="sxs-lookup"><span data-stu-id="fa1e3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1e3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa1e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa1e3-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa1e3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa1e3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa1e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa1e3-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa1e3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa1e3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fa1e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa1e3-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fa1e3-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa1e3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa1e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1e3-123">波形音訊</span><span class="sxs-lookup"><span data-stu-id="fa1e3-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="fa1e3-124">波形訊息</span><span class="sxs-lookup"><span data-stu-id="fa1e3-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





