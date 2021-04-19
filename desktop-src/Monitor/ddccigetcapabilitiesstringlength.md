---
title: DDCCIGetCapabilitiesStringLength 函式
description: 取得監視器之功能字串的長度。
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- DDCCIGetCapabilitiesStringLength 函式監視設定
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969962"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="c6613-104">DDCCIGetCapabilitiesStringLength 函式</span><span class="sxs-lookup"><span data-stu-id="c6613-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6613-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="c6613-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="c6613-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="c6613-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="c6613-107">取得監視器之功能字串的長度。</span><span class="sxs-lookup"><span data-stu-id="c6613-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6613-108">語法</span><span class="sxs-lookup"><span data-stu-id="c6613-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="c6613-109">參數</span><span class="sxs-lookup"><span data-stu-id="c6613-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6613-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6613-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6613-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6613-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c6613-112">*pdwLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6613-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6613-113">接收功能字串的長度（以字元為單位），包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="c6613-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6613-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6613-114">Return value</span></span>

<span data-ttu-id="c6613-115">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="c6613-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c6613-116">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6613-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6613-117">備註</span><span class="sxs-lookup"><span data-stu-id="c6613-117">Remarks</span></span>

<span data-ttu-id="c6613-118">應用程式應該呼叫 [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="c6613-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="c6613-119">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="c6613-119">This function has no associated import library.</span></span> <span data-ttu-id="c6613-120">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="c6613-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6613-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6613-121">Requirements</span></span>



| <span data-ttu-id="c6613-122">需求</span><span class="sxs-lookup"><span data-stu-id="c6613-122">Requirement</span></span> | <span data-ttu-id="c6613-123">值</span><span class="sxs-lookup"><span data-stu-id="c6613-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6613-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6613-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6613-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6613-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6613-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6613-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6613-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6613-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6613-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c6613-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6613-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6613-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6613-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6613-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6613-131">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="c6613-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

