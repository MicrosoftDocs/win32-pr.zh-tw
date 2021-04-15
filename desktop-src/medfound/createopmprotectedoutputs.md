---
description: 為顯示裝置建立受保護的輸出物件。
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510816"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="829cb-103">CreateOPMProtectedOutputs 函式</span><span class="sxs-lookup"><span data-stu-id="829cb-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="829cb-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="829cb-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="829cb-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="829cb-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="829cb-106">為顯示裝置建立受保護的輸出物件。</span><span class="sxs-lookup"><span data-stu-id="829cb-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="829cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="829cb-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="829cb-108">參數</span><span class="sxs-lookup"><span data-stu-id="829cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829cb-109">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="829cb-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829cb-110">[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="829cb-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="829cb-111">*vos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="829cb-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829cb-112">**DXGKMDT \_ OPM \_ VIDEO \_ output \_ 語義** 列舉的成員，指定受保護的輸出是否會有認證的輸出保護通訊協定 (COPP) 語義或 OPM 語義。</span><span class="sxs-lookup"><span data-stu-id="829cb-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="829cb-113">*dwOPMProtectedOutputArraySize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="829cb-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829cb-114">*PohOPMProtectedOutputArray* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="829cb-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="829cb-115">*pdwNumOPMProtectedOutputsInArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="829cb-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="829cb-116">接收函數複製到 *pohOPMProtectedOutputArray* 陣列的專案數。</span><span class="sxs-lookup"><span data-stu-id="829cb-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="829cb-117">*pohOPMProtectedOutputArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="829cb-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="829cb-118">接收受保護輸出物件之控制碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="829cb-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="829cb-119">每個控制碼都必須藉由呼叫 [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md)來釋放。</span><span class="sxs-lookup"><span data-stu-id="829cb-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829cb-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="829cb-120">Return value</span></span>

<span data-ttu-id="829cb-121">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="829cb-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="829cb-122">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="829cb-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="829cb-123">備註</span><span class="sxs-lookup"><span data-stu-id="829cb-123">Remarks</span></span>

<span data-ttu-id="829cb-124">應用程式應該呼叫下列其中一項功能，而不是使用此函式：</span><span class="sxs-lookup"><span data-stu-id="829cb-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="829cb-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="829cb-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="829cb-126">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="829cb-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="829cb-127">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="829cb-127">This function has no associated import library.</span></span> <span data-ttu-id="829cb-128">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="829cb-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="829cb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="829cb-129">Requirements</span></span>



| <span data-ttu-id="829cb-130">需求</span><span class="sxs-lookup"><span data-stu-id="829cb-130">Requirement</span></span> | <span data-ttu-id="829cb-131">值</span><span class="sxs-lookup"><span data-stu-id="829cb-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="829cb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="829cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="829cb-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="829cb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="829cb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="829cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="829cb-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="829cb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="829cb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="829cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="829cb-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="829cb-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829cb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="829cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829cb-139">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="829cb-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="829cb-140">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="829cb-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
