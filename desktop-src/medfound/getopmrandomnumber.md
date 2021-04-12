---
description: 從受保護的輸出物件取得128位、密碼編譯安全的亂數字。
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: GetOPMRandomNumber 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317956"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="a38a1-103">GetOPMRandomNumber 函式</span><span class="sxs-lookup"><span data-stu-id="a38a1-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a38a1-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="a38a1-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="a38a1-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="a38a1-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="a38a1-106">從受保護的輸出物件取得128位、密碼編譯安全的亂數字。</span><span class="sxs-lookup"><span data-stu-id="a38a1-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38a1-107">語法</span><span class="sxs-lookup"><span data-stu-id="a38a1-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="a38a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="a38a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38a1-109">*opoOPMProtectedOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a38a1-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a1-110">受保護之輸出物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a38a1-110">A handle to the protected output object.</span></span> <span data-ttu-id="a38a1-111">藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="a38a1-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38a1-112">*prnRandomNumber* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a38a1-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a1-113">**DXGKMDT \_ OPM \_ 亂數 \_** 結構的指標，該結構會接收亂數字。</span><span class="sxs-lookup"><span data-stu-id="a38a1-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38a1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a38a1-114">Return value</span></span>

<span data-ttu-id="a38a1-115">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="a38a1-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a38a1-116">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a38a1-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="a38a1-117">Remarks</span></span>

<span data-ttu-id="a38a1-118">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a38a1-118">This function has no associated import library.</span></span> <span data-ttu-id="a38a1-119">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="a38a1-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38a1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a38a1-120">Requirements</span></span>



| <span data-ttu-id="a38a1-121">需求</span><span class="sxs-lookup"><span data-stu-id="a38a1-121">Requirement</span></span> | <span data-ttu-id="a38a1-122">值</span><span class="sxs-lookup"><span data-stu-id="a38a1-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a38a1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a38a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a38a1-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a38a1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a38a1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a38a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a38a1-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a38a1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a38a1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a38a1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a38a1-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a38a1-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38a1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a38a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38a1-130">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="a38a1-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="a38a1-131">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="a38a1-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
