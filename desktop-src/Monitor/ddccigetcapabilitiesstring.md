---
title: DDCCIGetCapabilitiesString 函式
description: 取得描述監視功能的字串。
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- DDCCIGetCapabilitiesString 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965714"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="65cc0-104">DDCCIGetCapabilitiesString 函式</span><span class="sxs-lookup"><span data-stu-id="65cc0-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65cc0-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="65cc0-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="65cc0-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="65cc0-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="65cc0-107">取得描述監視功能的字串。</span><span class="sxs-lookup"><span data-stu-id="65cc0-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="65cc0-108">語法</span><span class="sxs-lookup"><span data-stu-id="65cc0-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="65cc0-109">參數</span><span class="sxs-lookup"><span data-stu-id="65cc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65cc0-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65cc0-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65cc0-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65cc0-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="65cc0-112">*pszString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="65cc0-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65cc0-113">接收功能字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="65cc0-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="65cc0-114">若要取得功能字串的長度，請呼叫 [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)。</span><span class="sxs-lookup"><span data-stu-id="65cc0-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="65cc0-115">*dwLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65cc0-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65cc0-116">*PszString* 緩衝區的大小（以字元為單位），包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="65cc0-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65cc0-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="65cc0-117">Return value</span></span>

<span data-ttu-id="65cc0-118">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="65cc0-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="65cc0-119">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65cc0-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65cc0-120">備註</span><span class="sxs-lookup"><span data-stu-id="65cc0-120">Remarks</span></span>

<span data-ttu-id="65cc0-121">應用程式應該呼叫 [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="65cc0-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="65cc0-122">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="65cc0-122">This function has no associated import library.</span></span> <span data-ttu-id="65cc0-123">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="65cc0-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="65cc0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="65cc0-124">Requirements</span></span>



| <span data-ttu-id="65cc0-125">需求</span><span class="sxs-lookup"><span data-stu-id="65cc0-125">Requirement</span></span> | <span data-ttu-id="65cc0-126">值</span><span class="sxs-lookup"><span data-stu-id="65cc0-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65cc0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65cc0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65cc0-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65cc0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="65cc0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65cc0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65cc0-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65cc0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="65cc0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="65cc0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65cc0-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65cc0-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65cc0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65cc0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65cc0-134">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="65cc0-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

