---
description: 在受保護的輸出物件上設定簽署金鑰和兩個序號。
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: SetOPMSigningKeyAndSequenceNumbers 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191752"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="63e4b-103">SetOPMSigningKeyAndSequenceNumbers 函式</span><span class="sxs-lookup"><span data-stu-id="63e4b-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63e4b-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="63e4b-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="63e4b-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="63e4b-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="63e4b-106">在受保護的輸出物件上設定簽署金鑰和兩個序號。</span><span class="sxs-lookup"><span data-stu-id="63e4b-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e4b-107">語法</span><span class="sxs-lookup"><span data-stu-id="63e4b-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="63e4b-108">參數</span><span class="sxs-lookup"><span data-stu-id="63e4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e4b-109">*opoOPMProtectedOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63e4b-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4b-110">受保護之輸出物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="63e4b-110">A handle to the protected output object.</span></span> <span data-ttu-id="63e4b-111">藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="63e4b-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="63e4b-112">*pParameters* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="63e4b-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4b-113">包含256位元組陣列的 [**DXGKMDT \_ OPM \_ 加密 \_ 參數**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="63e4b-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="63e4b-114">如需如何初始化此陣列的詳細資訊，請參閱 [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx)。</span><span class="sxs-lookup"><span data-stu-id="63e4b-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e4b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="63e4b-115">Return value</span></span>

<span data-ttu-id="63e4b-116">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="63e4b-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="63e4b-117">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="63e4b-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e4b-118">備註</span><span class="sxs-lookup"><span data-stu-id="63e4b-118">Remarks</span></span>

<span data-ttu-id="63e4b-119">應用程式應該呼叫 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="63e4b-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="63e4b-120">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="63e4b-120">This function has no associated import library.</span></span> <span data-ttu-id="63e4b-121">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="63e4b-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e4b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="63e4b-122">Requirements</span></span>



| <span data-ttu-id="63e4b-123">需求</span><span class="sxs-lookup"><span data-stu-id="63e4b-123">Requirement</span></span> | <span data-ttu-id="63e4b-124">值</span><span class="sxs-lookup"><span data-stu-id="63e4b-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63e4b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63e4b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63e4b-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63e4b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="63e4b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63e4b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63e4b-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63e4b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63e4b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="63e4b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e4b-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e4b-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e4b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63e4b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e4b-132">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="63e4b-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="63e4b-133">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="63e4b-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
