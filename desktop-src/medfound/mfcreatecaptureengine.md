---
description: 建立 capture 引擎的實例。
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996613"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="0389f-103">MFCreateCaptureEngine 函式</span><span class="sxs-lookup"><span data-stu-id="0389f-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="0389f-104">\[MFCreateCaptureEngine 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0389f-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0389f-105">\]</span><span class="sxs-lookup"><span data-stu-id="0389f-105">\]</span></span>

<span data-ttu-id="0389f-106">建立 capture 引擎的實例。</span><span class="sxs-lookup"><span data-stu-id="0389f-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0389f-107">語法</span><span class="sxs-lookup"><span data-stu-id="0389f-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="0389f-108">參數</span><span class="sxs-lookup"><span data-stu-id="0389f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0389f-109">*ppCaptureEngine* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0389f-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0389f-110">接收 [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0389f-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="0389f-111">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="0389f-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0389f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0389f-112">Return value</span></span>

<span data-ttu-id="0389f-113">如果函式成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0389f-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0389f-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0389f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0389f-115">備註</span><span class="sxs-lookup"><span data-stu-id="0389f-115">Remarks</span></span>

<span data-ttu-id="0389f-116">此函式沒有相關聯的匯入程式庫，且未在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="0389f-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="0389f-117">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 MFCaptureEngine.dll。</span><span class="sxs-lookup"><span data-stu-id="0389f-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0389f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0389f-118">Requirements</span></span>



| <span data-ttu-id="0389f-119">需求</span><span class="sxs-lookup"><span data-stu-id="0389f-119">Requirement</span></span> | <span data-ttu-id="0389f-120">值</span><span class="sxs-lookup"><span data-stu-id="0389f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0389f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0389f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0389f-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0389f-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0389f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0389f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0389f-124">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0389f-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0389f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0389f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0389f-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0389f-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0389f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0389f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0389f-128">媒體基礎函式</span><span class="sxs-lookup"><span data-stu-id="0389f-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
