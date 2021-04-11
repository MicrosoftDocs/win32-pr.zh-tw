---
description: 將認證的輸出保護通訊協定 (COPP) 狀態要求傳送到受保護的輸出物件。
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: GetCOPPCompatibleOPMInformation 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191052"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="53dcb-103">GetCOPPCompatibleOPMInformation 函式</span><span class="sxs-lookup"><span data-stu-id="53dcb-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53dcb-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="53dcb-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="53dcb-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53dcb-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="53dcb-106">將認證的輸出保護通訊協定 (COPP) 狀態要求傳送到受保護的輸出物件。</span><span class="sxs-lookup"><span data-stu-id="53dcb-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="53dcb-107">語法</span><span class="sxs-lookup"><span data-stu-id="53dcb-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="53dcb-108">參數</span><span class="sxs-lookup"><span data-stu-id="53dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53dcb-109">*opoOPMProtectedOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53dcb-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53dcb-110">受保護之輸出物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53dcb-110">A handle to the protected output object.</span></span> <span data-ttu-id="53dcb-111">藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="53dcb-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="53dcb-112">*pParameters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53dcb-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53dcb-113">**DXGKMDT \_ OPM \_ COPP \_ 相容的 \_ GET \_ INFO \_ 參數** 結構的指標，其中包含狀態要求的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="53dcb-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="53dcb-114">*pRequestedInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53dcb-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53dcb-115">DXGKMDT OPM 的指標，其 **\_ 要求的 \_ \_ 資訊** 結構會接收狀態要求的結果。</span><span class="sxs-lookup"><span data-stu-id="53dcb-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53dcb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="53dcb-116">Return value</span></span>

<span data-ttu-id="53dcb-117">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="53dcb-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="53dcb-118">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53dcb-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53dcb-119">備註</span><span class="sxs-lookup"><span data-stu-id="53dcb-119">Remarks</span></span>

<span data-ttu-id="53dcb-120">應用程式應該呼叫 [**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53dcb-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="53dcb-121">您必須使用 COPP 語義來建立受保護的輸出物件。</span><span class="sxs-lookup"><span data-stu-id="53dcb-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="53dcb-122">請參閱 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)。</span><span class="sxs-lookup"><span data-stu-id="53dcb-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="53dcb-123">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="53dcb-123">This function has no associated import library.</span></span> <span data-ttu-id="53dcb-124">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="53dcb-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="53dcb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="53dcb-125">Requirements</span></span>



| <span data-ttu-id="53dcb-126">需求</span><span class="sxs-lookup"><span data-stu-id="53dcb-126">Requirement</span></span> | <span data-ttu-id="53dcb-127">值</span><span class="sxs-lookup"><span data-stu-id="53dcb-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53dcb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53dcb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53dcb-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53dcb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="53dcb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53dcb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53dcb-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53dcb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="53dcb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="53dcb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53dcb-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53dcb-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53dcb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53dcb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53dcb-135">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="53dcb-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="53dcb-136">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="53dcb-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
