---
title: 'TS_SS_ 常數 (Textstor) '
description: Ts \_ SS \_ \ 常數（定義于 ts 狀態結構的執行時間之前 \_ ）會描述靜態檔狀態。
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967314"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="e620c-103">TS \_ SS \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="e620c-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="e620c-104">Ts \_ SS \_ \* 常數（定義于 [**ts \_ 狀態**](/windows/desktop/api/Textstor/ns-textstor-ts_status)結構的執行時間之前）會描述靜態檔狀態。</span><span class="sxs-lookup"><span data-stu-id="e620c-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="e620c-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="e620c-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="e620c-106">Description</span><span class="sxs-lookup"><span data-stu-id="e620c-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="e620c-107"><dt>**TS \_SS \_ DISJOINTSEL**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="e620c-108">此檔支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="e620c-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="e620c-109"><dt>**TS \_SS \_ 區域**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="e620c-110">檔可包含多個區域。</span><span class="sxs-lookup"><span data-stu-id="e620c-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="e620c-111"><dt>**TS \_SS \_ 暫時性**</dt> <dt> ( 0x4 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="e620c-112">檔預期會有簡短的使用週期。</span><span class="sxs-lookup"><span data-stu-id="e620c-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="e620c-113"><dt>**TS \_SS \_ NOHIDDENTEXT**</dt> <dt> ( 0x8 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="e620c-114">檔絕不會包含隱藏文字。</span><span class="sxs-lookup"><span data-stu-id="e620c-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="e620c-115"><dt>**TS \_SS \_ TKBAUTOCORRECTENABLE**</dt> <dt> ( 0x10 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="e620c-116">**從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的自動校正。</span><span class="sxs-lookup"><span data-stu-id="e620c-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="e620c-117"><dt>**TS \_SS \_ TKBPREDICTIONENABLE**</dt> <dt> ( 0x20 )</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="e620c-118">**從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的文字建議。</span><span class="sxs-lookup"><span data-stu-id="e620c-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e620c-119">備註</span><span class="sxs-lookup"><span data-stu-id="e620c-119">Remarks</span></span>

<span data-ttu-id="e620c-120">**TS \_ 狀態** 結構的 **dwStaticFlags** 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="e620c-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="e620c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e620c-121">Requirements</span></span>



| <span data-ttu-id="e620c-122">需求</span><span class="sxs-lookup"><span data-stu-id="e620c-122">Requirement</span></span> | <span data-ttu-id="e620c-123">值</span><span class="sxs-lookup"><span data-stu-id="e620c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e620c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e620c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e620c-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e620c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e620c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e620c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e620c-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e620c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e620c-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e620c-128">Redistributable</span></span><br/>          | <span data-ttu-id="e620c-129">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="e620c-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="e620c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e620c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e620c-131"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="e620c-132">Idl</span><span class="sxs-lookup"><span data-stu-id="e620c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e620c-133"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e620c-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e620c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e620c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e620c-135">**TS \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e620c-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="e620c-136">[**TF \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e620c-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

