---
title: DDCCIGetVCPFeature 函式
description: 取得虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- DDCCIGetVCPFeature 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934348"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="253f7-104">DDCCIGetVCPFeature 函式</span><span class="sxs-lookup"><span data-stu-id="253f7-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="253f7-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="253f7-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="253f7-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="253f7-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="253f7-107">取得虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。</span><span class="sxs-lookup"><span data-stu-id="253f7-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="253f7-108">語法</span><span class="sxs-lookup"><span data-stu-id="253f7-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="253f7-109">參數</span><span class="sxs-lookup"><span data-stu-id="253f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="253f7-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="253f7-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253f7-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="253f7-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="253f7-112">*dwVCPCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="253f7-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253f7-113">要查詢的 VCP 程式碼。</span><span class="sxs-lookup"><span data-stu-id="253f7-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="253f7-114">*pvct* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="253f7-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="253f7-115">以 [**MC \_ VCP 程式 \_ 代碼 \_ 類型**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) 列舉的成員形式接收 VCP 程式碼類型。</span><span class="sxs-lookup"><span data-stu-id="253f7-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="253f7-116">*pdwCurrentValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="253f7-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="253f7-117">接收 VCP 程式碼的目前值。</span><span class="sxs-lookup"><span data-stu-id="253f7-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="253f7-118">*pdwMaximumValue* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="253f7-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="253f7-119">接收 VCP 程式碼的最大值。</span><span class="sxs-lookup"><span data-stu-id="253f7-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="253f7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="253f7-120">Return value</span></span>

<span data-ttu-id="253f7-121">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="253f7-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="253f7-122">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="253f7-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="253f7-123">備註</span><span class="sxs-lookup"><span data-stu-id="253f7-123">Remarks</span></span>

<span data-ttu-id="253f7-124">應用程式應該呼叫 [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="253f7-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="253f7-125">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="253f7-125">This function has no associated import library.</span></span> <span data-ttu-id="253f7-126">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="253f7-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="253f7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="253f7-127">Requirements</span></span>



| <span data-ttu-id="253f7-128">需求</span><span class="sxs-lookup"><span data-stu-id="253f7-128">Requirement</span></span> | <span data-ttu-id="253f7-129">值</span><span class="sxs-lookup"><span data-stu-id="253f7-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="253f7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="253f7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="253f7-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="253f7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="253f7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="253f7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="253f7-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="253f7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="253f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="253f7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="253f7-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="253f7-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253f7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="253f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253f7-137">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="253f7-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

