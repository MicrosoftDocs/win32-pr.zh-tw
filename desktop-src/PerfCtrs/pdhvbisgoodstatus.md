---
description: PdhVbIsGoodStatus 函式會測試狀態值，以判斷其是否為成功或失敗的程式碼。 如果狀態值為成功，則傳回值將為非零值。 如果這是失敗狀態碼，傳回值將會是零。
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986938"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="b7744-105">PdhVbIsGoodStatus 函式</span><span class="sxs-lookup"><span data-stu-id="b7744-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="b7744-106">**PdhVbIsGoodStatus** 函式會測試狀態值，以判斷其是否為成功或失敗的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b7744-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="b7744-107">如果狀態值為成功，則傳回值將為非零值。</span><span class="sxs-lookup"><span data-stu-id="b7744-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="b7744-108">如果這是失敗狀態碼，傳回值將會是零。</span><span class="sxs-lookup"><span data-stu-id="b7744-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7744-109">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b7744-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="b7744-110">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="b7744-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="b7744-111">函式 PdhVbIsGoodStatus ( \_ ByVal StatusValue long \_ ) long</span><span class="sxs-lookup"><span data-stu-id="b7744-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="b7744-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7744-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7744-113">*StatusValue*</span><span class="sxs-lookup"><span data-stu-id="b7744-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="b7744-114">要測試的另一個 PDH 函數所傳回的狀態值。</span><span class="sxs-lookup"><span data-stu-id="b7744-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7744-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7744-115">Return value</span></span>

<span data-ttu-id="b7744-116">如果狀態碼為失敗狀態碼，則函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b7744-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="b7744-117">如果狀態碼為成功狀態碼，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="b7744-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7744-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7744-118">Requirements</span></span>



| <span data-ttu-id="b7744-119">需求</span><span class="sxs-lookup"><span data-stu-id="b7744-119">Requirement</span></span> | <span data-ttu-id="b7744-120">值</span><span class="sxs-lookup"><span data-stu-id="b7744-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7744-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7744-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7744-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7744-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7744-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7744-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7744-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7744-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7744-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7744-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7744-126"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7744-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7744-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b7744-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7744-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7744-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7744-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7744-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7744-130">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="b7744-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




