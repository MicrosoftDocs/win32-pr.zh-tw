---
title: DDCCIGetTimingReport 函式
description: 取得監視器的水準和垂直同步處理頻率。
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- DDCCIGetTimingReport 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934349"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="d7196-104">DDCCIGetTimingReport 函式</span><span class="sxs-lookup"><span data-stu-id="d7196-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7196-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="d7196-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="d7196-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="d7196-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="d7196-107">取得監視器的水準和垂直同步處理頻率。</span><span class="sxs-lookup"><span data-stu-id="d7196-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7196-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7196-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="d7196-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7196-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7196-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7196-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7196-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7196-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d7196-112">*pmtr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d7196-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7196-113">可接收計時資訊之 [**MC \_ 計時 \_ 報表**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d7196-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7196-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7196-114">Return value</span></span>

<span data-ttu-id="d7196-115">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="d7196-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d7196-116">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7196-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7196-117">備註</span><span class="sxs-lookup"><span data-stu-id="d7196-117">Remarks</span></span>

<span data-ttu-id="d7196-118">應用程式應該呼叫 [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="d7196-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="d7196-119">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="d7196-119">This function has no associated import library.</span></span> <span data-ttu-id="d7196-120">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="d7196-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7196-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7196-121">Requirements</span></span>



| <span data-ttu-id="d7196-122">需求</span><span class="sxs-lookup"><span data-stu-id="d7196-122">Requirement</span></span> | <span data-ttu-id="d7196-123">值</span><span class="sxs-lookup"><span data-stu-id="d7196-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7196-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7196-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7196-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7196-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7196-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7196-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7196-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7196-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7196-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d7196-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7196-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7196-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7196-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7196-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7196-131">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="d7196-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

