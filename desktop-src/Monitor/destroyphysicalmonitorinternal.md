---
title: DestroyPhysicalMonitorInternal 函式
description: 關閉實體監視器的控制碼。
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- DestroyPhysicalMonitorInternal 函式監視設定
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843527"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="19d90-104">DestroyPhysicalMonitorInternal 函式</span><span class="sxs-lookup"><span data-stu-id="19d90-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19d90-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="19d90-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="19d90-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="19d90-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="19d90-107">關閉實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="19d90-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d90-108">語法</span><span class="sxs-lookup"><span data-stu-id="19d90-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="19d90-109">參數</span><span class="sxs-lookup"><span data-stu-id="19d90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d90-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19d90-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d90-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="19d90-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d90-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="19d90-112">Return value</span></span>

<span data-ttu-id="19d90-113">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="19d90-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="19d90-114">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19d90-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d90-115">備註</span><span class="sxs-lookup"><span data-stu-id="19d90-115">Remarks</span></span>

<span data-ttu-id="19d90-116">應用程式應該呼叫 [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="19d90-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="19d90-117">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="19d90-117">This function has no associated import library.</span></span> <span data-ttu-id="19d90-118">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="19d90-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d90-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19d90-119">Requirements</span></span>



| <span data-ttu-id="19d90-120">需求</span><span class="sxs-lookup"><span data-stu-id="19d90-120">Requirement</span></span> | <span data-ttu-id="19d90-121">值</span><span class="sxs-lookup"><span data-stu-id="19d90-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19d90-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19d90-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19d90-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19d90-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="19d90-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19d90-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19d90-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19d90-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19d90-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19d90-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d90-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d90-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d90-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19d90-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d90-129">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="19d90-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

