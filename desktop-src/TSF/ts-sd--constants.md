---
title: 'TS_SD_ 常數 (Textstor) '
description: TS \_ SD \_ \ 常數描述應用程式在執行時間所使用的動態檔狀態。
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991122"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="ec658-103">TS \_ SD \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="ec658-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="ec658-104">TS \_ SD \_ \* 常數描述應用程式在執行時間所使用的動態檔狀態。</span><span class="sxs-lookup"><span data-stu-id="ec658-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="ec658-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ec658-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="ec658-106">Description</span><span class="sxs-lookup"><span data-stu-id="ec658-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="ec658-107"><dt>**TS \_SD \_ READONLY**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="ec658-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="ec658-108">檔是唯讀的，而且無法修改。</span><span class="sxs-lookup"><span data-stu-id="ec658-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="ec658-109"><dt>**TS \_SD \_**</dt> <dt>)  ( 0x2</dt>載入</span><span class="sxs-lookup"><span data-stu-id="ec658-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="ec658-110">檔正在載入，而且可能不完整。</span><span class="sxs-lookup"><span data-stu-id="ec658-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="ec658-111"><dt>**TS \_SD \_ MASKALL**</dt> <dt> ( ts \_ sd \_ READONLY \| ts \_ sd \_ ) 的載入</dt></span><span class="sxs-lookup"><span data-stu-id="ec658-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="ec658-112">檔是唯讀和載入的。</span><span class="sxs-lookup"><span data-stu-id="ec658-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="ec658-113">備註</span><span class="sxs-lookup"><span data-stu-id="ec658-113">Remarks</span></span>

<span data-ttu-id="ec658-114">[TS \_ 狀態](/windows/desktop/api/Textstor/ns-textstor-ts_status)結構的 **dwDynamicFlags** 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="ec658-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec658-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec658-115">Requirements</span></span>



| <span data-ttu-id="ec658-116">需求</span><span class="sxs-lookup"><span data-stu-id="ec658-116">Requirement</span></span> | <span data-ttu-id="ec658-117">值</span><span class="sxs-lookup"><span data-stu-id="ec658-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec658-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec658-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec658-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec658-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ec658-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec658-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec658-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec658-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec658-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ec658-122">Redistributable</span></span><br/>          | <span data-ttu-id="ec658-123">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="ec658-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ec658-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ec658-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec658-125"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec658-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec658-126">Idl</span><span class="sxs-lookup"><span data-stu-id="ec658-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec658-127"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec658-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec658-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec658-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec658-129">TS \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="ec658-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="ec658-130">TF \_ SD \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="ec658-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





