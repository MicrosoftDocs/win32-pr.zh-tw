---
title: GetNumberOfPhysicalMonitors 函式
description: 取得與顯示裝置相關聯的實體監視器數目。
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- GetNumberOfPhysicalMonitors 函式監視設定
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843524"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="04740-104">GetNumberOfPhysicalMonitors 函式</span><span class="sxs-lookup"><span data-stu-id="04740-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04740-105">監視器設定 API 會使用此函式來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="04740-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="04740-106">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="04740-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="04740-107">取得與顯示裝置相關聯的實體監視器數目。</span><span class="sxs-lookup"><span data-stu-id="04740-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="04740-108">語法</span><span class="sxs-lookup"><span data-stu-id="04740-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="04740-109">參數</span><span class="sxs-lookup"><span data-stu-id="04740-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04740-110">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04740-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04740-111">[**UNICODE \_ 字串**](/windows/desktop/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04740-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="04740-112">*pdwNumberOfPhysicalMonitors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04740-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04740-113">接收實體監視器的數目。</span><span class="sxs-lookup"><span data-stu-id="04740-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04740-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="04740-114">Return value</span></span>

<span data-ttu-id="04740-115">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="04740-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="04740-116">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="04740-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04740-117">備註</span><span class="sxs-lookup"><span data-stu-id="04740-117">Remarks</span></span>

<span data-ttu-id="04740-118">應用程式應該呼叫下列其中一項功能，而不是使用此函式：</span><span class="sxs-lookup"><span data-stu-id="04740-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="04740-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="04740-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="04740-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="04740-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="04740-121">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="04740-121">This function has no associated import library.</span></span> <span data-ttu-id="04740-122">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="04740-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="04740-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="04740-123">Requirements</span></span>



| <span data-ttu-id="04740-124">需求</span><span class="sxs-lookup"><span data-stu-id="04740-124">Requirement</span></span> | <span data-ttu-id="04740-125">值</span><span class="sxs-lookup"><span data-stu-id="04740-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04740-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04740-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04740-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04740-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="04740-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04740-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04740-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04740-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="04740-130">DLL</span><span class="sxs-lookup"><span data-stu-id="04740-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04740-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04740-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04740-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04740-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04740-133">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="04740-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

