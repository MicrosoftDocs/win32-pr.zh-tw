---
title: DDCCISetVCPFeature 函式
description: 設定監視的虛擬主控台 (VCP) 程式碼的值。
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- DDCCISetVCPFeature 函式監視設定
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094551"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="a2d60-104">DDCCISetVCPFeature 函式</span><span class="sxs-lookup"><span data-stu-id="a2d60-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2d60-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="a2d60-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="a2d60-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="a2d60-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="a2d60-107">設定監視的虛擬主控台 (VCP) 程式碼的值。</span><span class="sxs-lookup"><span data-stu-id="a2d60-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d60-108">語法</span><span class="sxs-lookup"><span data-stu-id="a2d60-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="a2d60-109">參數</span><span class="sxs-lookup"><span data-stu-id="a2d60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2d60-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2d60-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d60-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a2d60-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a2d60-112">*dwVCPCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2d60-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d60-113">要設定的 VCP 程式碼。</span><span class="sxs-lookup"><span data-stu-id="a2d60-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="a2d60-114">*dwNewValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2d60-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d60-115">VCP 碼的值。</span><span class="sxs-lookup"><span data-stu-id="a2d60-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2d60-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2d60-116">Return value</span></span>

<span data-ttu-id="a2d60-117">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="a2d60-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a2d60-118">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2d60-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d60-119">備註</span><span class="sxs-lookup"><span data-stu-id="a2d60-119">Remarks</span></span>

<span data-ttu-id="a2d60-120">應用程式應該呼叫 [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="a2d60-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="a2d60-121">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a2d60-121">This function has no associated import library.</span></span> <span data-ttu-id="a2d60-122">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="a2d60-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d60-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2d60-123">Requirements</span></span>



| <span data-ttu-id="a2d60-124">需求</span><span class="sxs-lookup"><span data-stu-id="a2d60-124">Requirement</span></span> | <span data-ttu-id="a2d60-125">值</span><span class="sxs-lookup"><span data-stu-id="a2d60-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d60-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2d60-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d60-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2d60-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a2d60-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2d60-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d60-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2d60-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2d60-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a2d60-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2d60-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2d60-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d60-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d60-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d60-133">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="a2d60-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

