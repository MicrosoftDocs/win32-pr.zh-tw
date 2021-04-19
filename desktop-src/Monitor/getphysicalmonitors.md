---
title: GetPhysicalMonitors 函式
description: 取得與顯示裝置相關聯的實體監視器。
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- GetPhysicalMonitors 函式監視設定
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967337"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="6c533-104">GetPhysicalMonitors 函式</span><span class="sxs-lookup"><span data-stu-id="6c533-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c533-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="6c533-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="6c533-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="6c533-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="6c533-107">取得與顯示裝置相關聯的實體監視器。</span><span class="sxs-lookup"><span data-stu-id="6c533-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c533-108">語法</span><span class="sxs-lookup"><span data-stu-id="6c533-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="6c533-109">參數</span><span class="sxs-lookup"><span data-stu-id="6c533-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c533-110">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c533-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c533-111">[**UNICODE \_ 字串**](/windows/desktop/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c533-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="6c533-112">*dwPhysicalMonitorArraySize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c533-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c533-113">*PdwNumPhysicalMonitorHandlesInArray* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6c533-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="6c533-114">若要取得陣列的所需大小，請呼叫 [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)。</span><span class="sxs-lookup"><span data-stu-id="6c533-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c533-115">*pdwNumPhysicalMonitorHandlesInArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c533-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c533-116">接收函數複製到 *phPhysicalMonitorArray* 陣列的專案數。</span><span class="sxs-lookup"><span data-stu-id="6c533-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="6c533-117">*phPhysicalMonitorArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c533-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c533-118">接收實體監視器之控制碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="6c533-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="6c533-119">每個控制碼都必須藉由呼叫 [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)來釋放。</span><span class="sxs-lookup"><span data-stu-id="6c533-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c533-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c533-120">Return value</span></span>

<span data-ttu-id="6c533-121">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="6c533-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="6c533-122">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c533-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c533-123">備註</span><span class="sxs-lookup"><span data-stu-id="6c533-123">Remarks</span></span>

<span data-ttu-id="6c533-124">應用程式應該呼叫下列其中一項功能，而不是使用此函式：</span><span class="sxs-lookup"><span data-stu-id="6c533-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="6c533-125">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="6c533-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="6c533-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="6c533-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="6c533-127">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="6c533-127">This function has no associated import library.</span></span> <span data-ttu-id="6c533-128">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="6c533-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c533-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c533-129">Requirements</span></span>



| <span data-ttu-id="6c533-130">需求</span><span class="sxs-lookup"><span data-stu-id="6c533-130">Requirement</span></span> | <span data-ttu-id="6c533-131">值</span><span class="sxs-lookup"><span data-stu-id="6c533-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c533-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c533-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6c533-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c533-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6c533-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c533-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6c533-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c533-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6c533-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6c533-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c533-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c533-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c533-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c533-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c533-139">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="6c533-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

