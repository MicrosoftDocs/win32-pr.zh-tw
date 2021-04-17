---
description: 通知 DWM 內送更新至視窗共用介面。
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface 函式
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512748"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="20cbd-103">DwmDxUpdateWindowSharedSurface 函式</span><span class="sxs-lookup"><span data-stu-id="20cbd-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="20cbd-104">通知 DWM 內送更新至視窗共用介面。</span><span class="sxs-lookup"><span data-stu-id="20cbd-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="20cbd-105">語法</span><span class="sxs-lookup"><span data-stu-id="20cbd-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="20cbd-106">參數</span><span class="sxs-lookup"><span data-stu-id="20cbd-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="20cbd-107">指定要更新之視窗的 [**HWND**](/windows/desktop/winprog/windows-data-types) 。</span><span class="sxs-lookup"><span data-stu-id="20cbd-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="20cbd-108">從 [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md)中取出的更新識別碼。</span><span class="sxs-lookup"><span data-stu-id="20cbd-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="20cbd-109">保留的。</span><span class="sxs-lookup"><span data-stu-id="20cbd-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="20cbd-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="20cbd-110">Reserved.</span></span>

`prc`

<span data-ttu-id="20cbd-111">要更新之視窗的矩形（在視窗座標空間中）。</span><span class="sxs-lookup"><span data-stu-id="20cbd-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="20cbd-112">Null 矩形表示未更新任何區域。</span><span class="sxs-lookup"><span data-stu-id="20cbd-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="20cbd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="20cbd-113">Return value</span></span>

<span data-ttu-id="20cbd-114">**S \_** 如果成功，則為 [確定]，否則為失敗的 **HRESULT。**</span><span class="sxs-lookup"><span data-stu-id="20cbd-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="20cbd-115">備註</span><span class="sxs-lookup"><span data-stu-id="20cbd-115">Remarks</span></span>

<span data-ttu-id="20cbd-116">此 API 適用于執行圖形驅動程式或執行時間。</span><span class="sxs-lookup"><span data-stu-id="20cbd-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="20cbd-117">應用程式可能不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="20cbd-117">An application may not call this method.</span></span> <span data-ttu-id="20cbd-118">本檔僅適用于 Windows 7，而且此 API 不保證存在，也不會在其他 Windows 版本上以類似的方式運作。</span><span class="sxs-lookup"><span data-stu-id="20cbd-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="20cbd-119">此函式不會出現在任何標頭或靜態程式庫中，而且位於 dwmapi.dll 的序數101。</span><span class="sxs-lookup"><span data-stu-id="20cbd-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="20cbd-120">只有在 [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) 傳回 **S \_ OK** 之後，才應該呼叫這個方法，而且必須在該情況下呼叫，不論介面是否更新。</span><span class="sxs-lookup"><span data-stu-id="20cbd-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cbd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="20cbd-121">Requirements</span></span>

| <span data-ttu-id="20cbd-122">需求</span><span class="sxs-lookup"><span data-stu-id="20cbd-122">Requirement</span></span> | <span data-ttu-id="20cbd-123">值</span><span class="sxs-lookup"><span data-stu-id="20cbd-123">Value</span></span> |
|-|-|
| <span data-ttu-id="20cbd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20cbd-124">Minimum supported client</span></span> | <span data-ttu-id="20cbd-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20cbd-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="20cbd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20cbd-126">Minimum supported server</span></span> | <span data-ttu-id="20cbd-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="20cbd-127">None supported</span></span> |
| <span data-ttu-id="20cbd-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="20cbd-128">End of client support</span></span> | <span data-ttu-id="20cbd-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20cbd-129">Windows 7</span></span> |
| <span data-ttu-id="20cbd-130">標頭</span><span class="sxs-lookup"><span data-stu-id="20cbd-130">Header</span></span> | <span data-ttu-id="20cbd-131">N/A</span><span class="sxs-lookup"><span data-stu-id="20cbd-131">N/A</span></span> |
| <span data-ttu-id="20cbd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="20cbd-132">DLL</span></span> | <span data-ttu-id="20cbd-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="20cbd-133">Dwmapi.dll</span></span> |
