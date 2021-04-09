---
title: 'MOM_OPEN 訊息 (Mmsystem .h) '
description: '\_開啟 midi 輸出裝置時，會將 MOM OPEN 訊息傳送至 midi 輸出回撥函式。'
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686373"
---
# <a name="mom_open-message"></a><span data-ttu-id="6c849-104">MOM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="6c849-104">MOM\_OPEN message</span></span>

<span data-ttu-id="6c849-105">開啟 MIDI 輸出裝置時，會將 **MOM \_ OPEN** 訊息傳送至 midi 輸出回撥函式。</span><span class="sxs-lookup"><span data-stu-id="6c849-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6c849-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c849-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6c849-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6c849-108">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="6c849-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="6c849-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6c849-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6c849-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="6c849-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c849-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c849-111">Return Value</span></span>

<span data-ttu-id="6c849-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c849-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c849-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c849-113">Requirements</span></span>



| <span data-ttu-id="6c849-114">需求</span><span class="sxs-lookup"><span data-stu-id="6c849-114">Requirement</span></span> | <span data-ttu-id="6c849-115">值</span><span class="sxs-lookup"><span data-stu-id="6c849-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c849-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c849-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c849-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c849-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c849-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c849-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c849-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c849-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c849-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6c849-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c849-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6c849-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c849-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c849-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c849-123">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="6c849-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





