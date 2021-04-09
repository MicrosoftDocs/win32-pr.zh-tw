---
title: DDCCISaveCurrentSettings 函式
description: 將目前的監視器設定儲存至顯示器的非動態儲存體。
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- DDCCISaveCurrentSettings 函式監視設定
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934177"
---
# <a name="ddccisavecurrentsettings-function"></a><span data-ttu-id="ed085-104">DDCCISaveCurrentSettings 函式</span><span class="sxs-lookup"><span data-stu-id="ed085-104">DDCCISaveCurrentSettings function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed085-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="ed085-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="ed085-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="ed085-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="ed085-107">將目前的監視器設定儲存至顯示器的非動態儲存體。</span><span class="sxs-lookup"><span data-stu-id="ed085-107">Saves the current monitor settings to the display's nonvolatile storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed085-108">語法</span><span class="sxs-lookup"><span data-stu-id="ed085-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="ed085-109">參數</span><span class="sxs-lookup"><span data-stu-id="ed085-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed085-110">*hMonitor*</span><span class="sxs-lookup"><span data-stu-id="ed085-110">*hMonitor*</span></span> 
</dt> <dd>

<span data-ttu-id="ed085-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed085-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed085-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed085-112">Return value</span></span>

<span data-ttu-id="ed085-113">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="ed085-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ed085-114">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ed085-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed085-115">備註</span><span class="sxs-lookup"><span data-stu-id="ed085-115">Remarks</span></span>

<span data-ttu-id="ed085-116">應用程式應該呼叫 [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="ed085-116">Applications should call [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) instead of calling this function.</span></span>

<span data-ttu-id="ed085-117">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="ed085-117">This function has no associated import library.</span></span> <span data-ttu-id="ed085-118">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="ed085-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed085-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed085-119">Requirements</span></span>



| <span data-ttu-id="ed085-120">需求</span><span class="sxs-lookup"><span data-stu-id="ed085-120">Requirement</span></span> | <span data-ttu-id="ed085-121">值</span><span class="sxs-lookup"><span data-stu-id="ed085-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed085-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed085-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed085-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed085-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ed085-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed085-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed085-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed085-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed085-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ed085-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed085-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed085-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed085-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed085-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed085-129">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="ed085-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

