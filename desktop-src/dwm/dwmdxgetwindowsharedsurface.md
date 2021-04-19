---
description: 抓取支援指定視窗的 DirectX 共用介面。 您可以將這個介面寫入，以便更新視窗的內容。
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface 函式
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969258"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="f1f51-104">DwmDxGetWindowSharedSurface 函式</span><span class="sxs-lookup"><span data-stu-id="f1f51-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="f1f51-105">抓取支援指定視窗的 DirectX 共用介面。</span><span class="sxs-lookup"><span data-stu-id="f1f51-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="f1f51-106">您可以將這個介面寫入，以便更新視窗的內容。</span><span class="sxs-lookup"><span data-stu-id="f1f51-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f51-107">語法</span><span class="sxs-lookup"><span data-stu-id="f1f51-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="f1f51-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1f51-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="f1f51-109">指定要更新之視窗的 [**HWND**](/windows/desktop/winprog/windows-data-types) 。</span><span class="sxs-lookup"><span data-stu-id="f1f51-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="f1f51-110">介面所在的介面卡的 [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="f1f51-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="f1f51-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="f1f51-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="f1f51-112">這個參數可以是下列其中一個值，或是在適當的情況下，多個值的位 OR 組合。</span><span class="sxs-lookup"><span data-stu-id="f1f51-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="f1f51-113">值</span><span class="sxs-lookup"><span data-stu-id="f1f51-113">Value</span></span> | <span data-ttu-id="f1f51-114">意義</span><span class="sxs-lookup"><span data-stu-id="f1f51-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="f1f51-115"><dt>**DWM \_重新導向 \_ 旗標 \_ 等候**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f1f51-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f1f51-116">導致函式封鎖，直到上次呼叫函式之後， (VSync) 已過為止。</span><span class="sxs-lookup"><span data-stu-id="f1f51-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="f1f51-117"><dt>**DWM \_\_ \_ \_ 存在 \_ 于 \_ GDI \_ 介面**</dt> <dt>0x10</dt>的重新導向旗標支援</span><span class="sxs-lookup"><span data-stu-id="f1f51-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="f1f51-118">指出呼叫的應用程式能夠向 GDI 共用介面呈現。</span><span class="sxs-lookup"><span data-stu-id="f1f51-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="f1f51-119">輸入時所需的介面格式。</span><span class="sxs-lookup"><span data-stu-id="f1f51-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="f1f51-120">在輸出時，傳回介面的實際格式。</span><span class="sxs-lookup"><span data-stu-id="f1f51-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="f1f51-121">在輸出時，為介面的共用控制碼。</span><span class="sxs-lookup"><span data-stu-id="f1f51-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="f1f51-122">在輸出時，更新的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1f51-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1f51-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1f51-123">Return value</span></span>

<span data-ttu-id="f1f51-124">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f1f51-124">This function can return one of these values.</span></span>

| <span data-ttu-id="f1f51-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1f51-125">Return code</span></span> | <span data-ttu-id="f1f51-126">Description</span><span class="sxs-lookup"><span data-stu-id="f1f51-126">Description</span></span> |
|-|-|
| <span data-ttu-id="f1f51-127">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="f1f51-127">**S\_OK**</span></span> | <span data-ttu-id="f1f51-128">呼叫成功，您應該更新介面，在提交更新時，請務必將更新識別碼傳遞至 D3DKMT 轉譯結構的 **PresentHistoryToken** 成員中 **的 \_** [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (，然後使用相同的更新識別碼來呼叫 [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) 。</span><span class="sxs-lookup"><span data-stu-id="f1f51-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="f1f51-129">請注意，不論是否已實際更新介面，都應該呼叫 **DwmDxUpdateWindowSharedSurface** 。</span><span class="sxs-lookup"><span data-stu-id="f1f51-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="f1f51-130">**DWM \_ S \_ GDI 重新導向 \_ \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="f1f51-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="f1f51-131">呼叫成功，您應該呼叫 [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)來更新介面，並將 **PresentHistoryToken** 成員的 **模型** 設定為 **D3DKMT PM 重新 \_ \_ 導向 \_ BLT**，並在聯集的 **BLT** 成員中提供更新識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1f51-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="f1f51-132">只有在 *dwFlags* 中指定了 **針對 \_ \_ \_ \_ \_ \_ GDI \_ 介面提供的 DWM** 重新導向旗標支援時，才會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="f1f51-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="f1f51-133">**\_ \_ \_ \_ 找不到 DWM E ADAPTER**</span><span class="sxs-lookup"><span data-stu-id="f1f51-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="f1f51-134">*LuidAdapter* 的值無效。</span><span class="sxs-lookup"><span data-stu-id="f1f51-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="f1f51-135">**DWM \_ E \_ COMPOSITIONDISABLED**</span><span class="sxs-lookup"><span data-stu-id="f1f51-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="f1f51-136">DWM 目前未啟用，且應用程式必須以另一種方式呈現。</span><span class="sxs-lookup"><span data-stu-id="f1f51-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f1f51-137">備註</span><span class="sxs-lookup"><span data-stu-id="f1f51-137">Remarks</span></span>

<span data-ttu-id="f1f51-138">此 API 適用于執行圖形驅動程式或執行時間。</span><span class="sxs-lookup"><span data-stu-id="f1f51-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="f1f51-139">應用程式可能不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1f51-139">An application may not call this method.</span></span> <span data-ttu-id="f1f51-140">本檔僅適用于 Windows 7，而且此 API 不保證存在，也不會在其他 Windows 版本上以類似的方式運作。</span><span class="sxs-lookup"><span data-stu-id="f1f51-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="f1f51-141">此函式不會出現在任何標頭或靜態程式庫中，而且位於 dwmapi.dll 的序數100。</span><span class="sxs-lookup"><span data-stu-id="f1f51-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f51-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1f51-142">Requirements</span></span>

| <span data-ttu-id="f1f51-143">需求</span><span class="sxs-lookup"><span data-stu-id="f1f51-143">Requirement</span></span> | <span data-ttu-id="f1f51-144">值</span><span class="sxs-lookup"><span data-stu-id="f1f51-144">Value</span></span> |
|-|-|
| <span data-ttu-id="f1f51-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1f51-145">Minimum supported client</span></span> | <span data-ttu-id="f1f51-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1f51-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="f1f51-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1f51-147">Minimum supported server</span></span> | <span data-ttu-id="f1f51-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="f1f51-148">None supported</span></span> |
| <span data-ttu-id="f1f51-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f1f51-149">End of client support</span></span> | <span data-ttu-id="f1f51-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1f51-150">Windows 7</span></span> |
| <span data-ttu-id="f1f51-151">標頭</span><span class="sxs-lookup"><span data-stu-id="f1f51-151">Header</span></span> | <span data-ttu-id="f1f51-152">N/A</span><span class="sxs-lookup"><span data-stu-id="f1f51-152">N/A</span></span> |
| <span data-ttu-id="f1f51-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f1f51-153">DLL</span></span> | <span data-ttu-id="f1f51-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="f1f51-154">Dwmapi.dll</span></span> |
