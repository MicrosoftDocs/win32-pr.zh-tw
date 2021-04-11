---
title: GetPhysicalMonitorDescription 函式
description: 取得實體監視器的描述。
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- GetPhysicalMonitorDescription 函式監視設定
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094548"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="81943-104">GetPhysicalMonitorDescription 函式</span><span class="sxs-lookup"><span data-stu-id="81943-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81943-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="81943-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="81943-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="81943-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="81943-107">取得實體監視器的描述。</span><span class="sxs-lookup"><span data-stu-id="81943-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="81943-108">語法</span><span class="sxs-lookup"><span data-stu-id="81943-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="81943-109">參數</span><span class="sxs-lookup"><span data-stu-id="81943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81943-110">*hMonitor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81943-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81943-111">實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="81943-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="81943-112">*dwPhysicalMonitorDescriptionSizeInChars* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81943-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81943-113">*SzPhysicalMonitorDescription* 陣列中的字元數。</span><span class="sxs-lookup"><span data-stu-id="81943-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="81943-114">*szPhysicalMonitorDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81943-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81943-115">接收描述的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="81943-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="81943-116">陣列中的元素數目至少應該是 **實體 \_ 監視器 \_ 描述的 \_ 大小**。</span><span class="sxs-lookup"><span data-stu-id="81943-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81943-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="81943-117">Return value</span></span>

<span data-ttu-id="81943-118">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="81943-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="81943-119">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="81943-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81943-120">備註</span><span class="sxs-lookup"><span data-stu-id="81943-120">Remarks</span></span>

<span data-ttu-id="81943-121">應用程式應該呼叫下列其中一項功能，而不是使用此函式：</span><span class="sxs-lookup"><span data-stu-id="81943-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="81943-122">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="81943-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="81943-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="81943-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="81943-124">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="81943-124">This function has no associated import library.</span></span> <span data-ttu-id="81943-125">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="81943-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="81943-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="81943-126">Requirements</span></span>



| <span data-ttu-id="81943-127">需求</span><span class="sxs-lookup"><span data-stu-id="81943-127">Requirement</span></span> | <span data-ttu-id="81943-128">值</span><span class="sxs-lookup"><span data-stu-id="81943-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81943-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81943-129">Minimum supported client</span></span><br/> | <span data-ttu-id="81943-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81943-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="81943-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81943-131">Minimum supported server</span></span><br/> | <span data-ttu-id="81943-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81943-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81943-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81943-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81943-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81943-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81943-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81943-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81943-136">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="81943-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

