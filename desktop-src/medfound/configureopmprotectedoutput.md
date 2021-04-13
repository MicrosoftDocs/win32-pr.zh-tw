---
description: 設定受保護的輸出物件。
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386044"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="d287a-103">ConfigureOPMProtectedOutput 函式</span><span class="sxs-lookup"><span data-stu-id="d287a-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d287a-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="d287a-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d287a-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="d287a-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d287a-106">設定受保護的輸出物件。</span><span class="sxs-lookup"><span data-stu-id="d287a-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d287a-107">語法</span><span class="sxs-lookup"><span data-stu-id="d287a-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="d287a-108">參數</span><span class="sxs-lookup"><span data-stu-id="d287a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d287a-109">*opoOPMProtectedOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d287a-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d287a-110">受保護之輸出物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d287a-110">A handle to the protected output object.</span></span> <span data-ttu-id="d287a-111">藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d287a-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="d287a-112">*pParameters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d287a-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d287a-113">DXGKMDT OPM 的指標，可設定包含 configuration 命令的 **\_ \_ \_ 參數** 結構。</span><span class="sxs-lookup"><span data-stu-id="d287a-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="d287a-114">*ulAdditionalParametersSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d287a-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d287a-115">*PbAdditionalParameters* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d287a-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d287a-116">*pbAdditionalParameters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d287a-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d287a-117">緩衝區的指標，其中包含命令的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d287a-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d287a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d287a-118">Return value</span></span>

<span data-ttu-id="d287a-119">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="d287a-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d287a-120">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d287a-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d287a-121">備註</span><span class="sxs-lookup"><span data-stu-id="d287a-121">Remarks</span></span>

<span data-ttu-id="d287a-122">應用程式應該呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) ，而不是呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="d287a-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="d287a-123">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="d287a-123">This function has no associated import library.</span></span> <span data-ttu-id="d287a-124">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="d287a-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d287a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d287a-125">Requirements</span></span>



| <span data-ttu-id="d287a-126">需求</span><span class="sxs-lookup"><span data-stu-id="d287a-126">Requirement</span></span> | <span data-ttu-id="d287a-127">值</span><span class="sxs-lookup"><span data-stu-id="d287a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d287a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d287a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d287a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d287a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d287a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d287a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d287a-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d287a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d287a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d287a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d287a-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d287a-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d287a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d287a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d287a-135">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="d287a-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d287a-136">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="d287a-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
