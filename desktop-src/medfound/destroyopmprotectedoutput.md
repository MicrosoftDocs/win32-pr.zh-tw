---
description: 釋放受保護的輸出物件。
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: DestroyOPMProtectedOutput 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991658"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="d7c1a-103">DestroyOPMProtectedOutput 函式</span><span class="sxs-lookup"><span data-stu-id="d7c1a-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7c1a-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d7c1a-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d7c1a-106">釋放受保護的輸出物件。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="d7c1a-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="d7c1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="d7c1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c1a-109">*opoOPMProtectedOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7c1a-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c1a-110">受保護之輸出物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-110">A handle to the protected output object.</span></span> <span data-ttu-id="d7c1a-111">藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c1a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7c1a-112">Return value</span></span>

<span data-ttu-id="d7c1a-113">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d7c1a-114">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7c1a-115">備註</span><span class="sxs-lookup"><span data-stu-id="d7c1a-115">Remarks</span></span>

<span data-ttu-id="d7c1a-116">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-116">This function has no associated import library.</span></span> <span data-ttu-id="d7c1a-117">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="d7c1a-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c1a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c1a-118">Requirements</span></span>



| <span data-ttu-id="d7c1a-119">需求</span><span class="sxs-lookup"><span data-stu-id="d7c1a-119">Requirement</span></span> | <span data-ttu-id="d7c1a-120">值</span><span class="sxs-lookup"><span data-stu-id="d7c1a-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c1a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7c1a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c1a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7c1a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7c1a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7c1a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c1a-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7c1a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7c1a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c1a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7c1a-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7c1a-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c1a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c1a-128">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="d7c1a-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d7c1a-129">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="d7c1a-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
