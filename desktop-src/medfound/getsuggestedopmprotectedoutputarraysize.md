---
description: 取得在呼叫 CreateOPMProtectedOutputs 之前，應該配置的陣列大小。
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111761"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="e0ab3-103">GetSuggestedOPMProtectedOutputArraySize 函式</span><span class="sxs-lookup"><span data-stu-id="e0ab3-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0ab3-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e0ab3-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e0ab3-106">取得在呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)之前，應該配置的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ab3-107">語法</span><span class="sxs-lookup"><span data-stu-id="e0ab3-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="e0ab3-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ab3-109">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0ab3-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ab3-110">[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e0ab3-111">*pdwSuggestedOPMProtectedOutputArraySize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e0ab3-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ab3-112">接收應配置給陣列的大小，以陣列元素的數目為限。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ab3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0ab3-113">Return value</span></span>

<span data-ttu-id="e0ab3-114">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e0ab3-115">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0ab3-116">備註</span><span class="sxs-lookup"><span data-stu-id="e0ab3-116">Remarks</span></span>

<span data-ttu-id="e0ab3-117">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-117">This function has no associated import library.</span></span> <span data-ttu-id="e0ab3-118">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="e0ab3-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ab3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0ab3-119">Requirements</span></span>



| <span data-ttu-id="e0ab3-120">需求</span><span class="sxs-lookup"><span data-stu-id="e0ab3-120">Requirement</span></span> | <span data-ttu-id="e0ab3-121">值</span><span class="sxs-lookup"><span data-stu-id="e0ab3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ab3-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0ab3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ab3-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0ab3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e0ab3-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0ab3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ab3-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0ab3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0ab3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ab3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ab3-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ab3-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ab3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0ab3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ab3-129">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="e0ab3-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e0ab3-130">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="e0ab3-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
