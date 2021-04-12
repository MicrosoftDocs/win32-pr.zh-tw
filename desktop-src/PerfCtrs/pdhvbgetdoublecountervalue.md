---
description: PdhVbGetDoubleCounterValue 函式會將指定計數器的目前值傳回為雙精確度浮點值。
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319180"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="795d5-103">PdhVbGetDoubleCounterValue 函式</span><span class="sxs-lookup"><span data-stu-id="795d5-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="795d5-104">**PdhVbGetDoubleCounterValue** 函式會將指定計數器的目前值傳回為雙精確度浮點值。</span><span class="sxs-lookup"><span data-stu-id="795d5-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="795d5-105">使用傳回的數位之前，您應該先檢查 *CounterStatus* ，因為計數器在讀取時可能無效。</span><span class="sxs-lookup"><span data-stu-id="795d5-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="795d5-106">若要檢查計數器狀態，請呼叫 [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="795d5-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="795d5-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="795d5-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="795d5-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="795d5-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="795d5-109">函式 PdhVbGetDoubleCounterValue ( \_ Byval CounterHandle long， \_ Byval CounterStatus 的 Long \_ ) 為 Double</span><span class="sxs-lookup"><span data-stu-id="795d5-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="795d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="795d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795d5-111">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="795d5-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="795d5-112">要讀取其目前值之計數器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="795d5-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-113">*CounterStatus*</span><span class="sxs-lookup"><span data-stu-id="795d5-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="795d5-114">變數，其中計數器值的目前狀態會傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="795d5-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="795d5-115">只有在 CounterStatus 中傳回的值為 PDH \_ CSTATUS 有效資料或 pdh CSTATUS 新資料時，傳回的資料值才有效， \_ \_ \_ \_ \_ (查看 pdh 錯誤碼) 。</span><span class="sxs-lookup"><span data-stu-id="795d5-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="795d5-116">如果 CounterStatus 中所傳回的值是任何其他值，請勿使用資料。</span><span class="sxs-lookup"><span data-stu-id="795d5-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795d5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="795d5-117">Return value</span></span>

<span data-ttu-id="795d5-118">此函數會傳回目前計數器的雙精確度浮點值（依計數器類型的定義計算和格式化）。</span><span class="sxs-lookup"><span data-stu-id="795d5-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="795d5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="795d5-119">Requirements</span></span>



| <span data-ttu-id="795d5-120">需求</span><span class="sxs-lookup"><span data-stu-id="795d5-120">Requirement</span></span> | <span data-ttu-id="795d5-121">值</span><span class="sxs-lookup"><span data-stu-id="795d5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="795d5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="795d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="795d5-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="795d5-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="795d5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="795d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="795d5-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="795d5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="795d5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="795d5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="795d5-127"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="795d5-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="795d5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="795d5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="795d5-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="795d5-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795d5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="795d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795d5-131">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="795d5-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




