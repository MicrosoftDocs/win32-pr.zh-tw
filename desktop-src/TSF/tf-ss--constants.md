---
title: 'TF_SS_ 常數 (Msctf) '
description: TF \_ SS \_ \ 常數，定義在 tf 狀態結構的執行時間之前 \_ ，會描述靜態檔狀態。
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025200"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="6baa0-103">TF \_ SS \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="6baa0-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="6baa0-104">TF \_ SS \_ \* 常數（定義在 [**tf \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))結構的執行時間之前）會描述靜態檔狀態。</span><span class="sxs-lookup"><span data-stu-id="6baa0-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="6baa0-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="6baa0-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="6baa0-106">Description</span><span class="sxs-lookup"><span data-stu-id="6baa0-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="6baa0-107"><dt>**TF \_SS \_ DISJOINTSEL**</dt> <dt> ( TS \_ SS \_ DISJOINTSEL )</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="6baa0-108">此檔支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="6baa0-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="6baa0-109"><dt>**TF \_SS \_ 區域**</dt> <dt> ( TS \_ SS \_ 區域 )</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="6baa0-110">檔可包含多個區域。</span><span class="sxs-lookup"><span data-stu-id="6baa0-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="6baa0-111"><dt>**TF \_SS \_ 暫時性**</dt> <dt> ( TS \_ SS \_ 暫時性 )</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="6baa0-112">檔預期會有簡短的使用週期。</span><span class="sxs-lookup"><span data-stu-id="6baa0-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="6baa0-113"><dt>**TF \_SS \_ TKBAUTOCORRECTENABLE**</dt> <dt> ( TS \_ SS \_ TKBAUTOCORRECTENABLE )</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="6baa0-114">**從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的自動校正。</span><span class="sxs-lookup"><span data-stu-id="6baa0-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="6baa0-115"><dt>**TF \_SS \_ TKBPREDICTIONENABLE**</dt> <dt> ( TS \_ SS \_ TKBPREDICTIONENABLE )</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="6baa0-116">**從 Windows 8 開始：** 此檔支援觸控鍵盤所提供的文字建議。</span><span class="sxs-lookup"><span data-stu-id="6baa0-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6baa0-117">備註</span><span class="sxs-lookup"><span data-stu-id="6baa0-117">Remarks</span></span>

<span data-ttu-id="6baa0-118">TF 狀態結構的 **dwStaticFlags** 成員會 \_ 使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="6baa0-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="6baa0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6baa0-119">Requirements</span></span>



| <span data-ttu-id="6baa0-120">需求</span><span class="sxs-lookup"><span data-stu-id="6baa0-120">Requirement</span></span> | <span data-ttu-id="6baa0-121">值</span><span class="sxs-lookup"><span data-stu-id="6baa0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6baa0-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6baa0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6baa0-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6baa0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6baa0-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6baa0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6baa0-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6baa0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6baa0-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6baa0-126">Redistributable</span></span><br/>          | <span data-ttu-id="6baa0-127">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="6baa0-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="6baa0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6baa0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6baa0-129"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="6baa0-130">Idl</span><span class="sxs-lookup"><span data-stu-id="6baa0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6baa0-131"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6baa0-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6baa0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6baa0-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="6baa0-133">[**TF \_ 狀態**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6baa0-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

