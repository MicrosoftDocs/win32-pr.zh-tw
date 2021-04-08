---
description: GetCaptureMacType 函式會傳回指定之捕捉的 MAC 型別。
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: 'GetCaptureMacType 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689724"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="fa665-103">GetCaptureMacType 函式</span><span class="sxs-lookup"><span data-stu-id="fa665-103">GetCaptureMacType function</span></span>

<span data-ttu-id="fa665-104">**GetCaptureMacType** 函式會傳回指定之捕捉的 MAC 型別。</span><span class="sxs-lookup"><span data-stu-id="fa665-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa665-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa665-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="fa665-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa665-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa665-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa665-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa665-108">Handle to the capture.</span></span> <span data-ttu-id="fa665-109">如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureMacType** 主題中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="fa665-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa665-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa665-110">Return value</span></span>

<span data-ttu-id="fa665-111">如果函式成功，則傳回值是下列其中一種 MAC 類型。</span><span class="sxs-lookup"><span data-stu-id="fa665-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="fa665-112">MAC \_ 類型 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="fa665-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="fa665-113">MAC \_ 類型 \_ ETHERNET</span><span class="sxs-lookup"><span data-stu-id="fa665-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="fa665-114">MAC \_ 類型 \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="fa665-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="fa665-115">MAC \_ 類型的 \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="fa665-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="fa665-116">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fa665-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="fa665-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fa665-117">Return code</span></span>                                                                                              | <span data-ttu-id="fa665-118">Description</span><span class="sxs-lookup"><span data-stu-id="fa665-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="fa665-119"><dt>**NMERR \_ MAC \_ 類型 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="fa665-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="fa665-120">網路監視器找不到已知的 MAC 類型。</span><span class="sxs-lookup"><span data-stu-id="fa665-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa665-121">備註</span><span class="sxs-lookup"><span data-stu-id="fa665-121">Remarks</span></span>

<span data-ttu-id="fa665-122">您可以透過數種方式取得 capture 的控制碼，視呼叫者而定。</span><span class="sxs-lookup"><span data-stu-id="fa665-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="fa665-123">對於專家而言，控制碼是在 [EXPERTSTARTUPINFO](expertstartupinfo.md)結構的 **hCapture** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="fa665-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="fa665-124">若為剖析器，可以藉由呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數來取得 capture 控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa665-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="fa665-125">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureMacType** 函數。</span><span class="sxs-lookup"><span data-stu-id="fa665-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa665-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa665-126">Requirements</span></span>



| <span data-ttu-id="fa665-127">需求</span><span class="sxs-lookup"><span data-stu-id="fa665-127">Requirement</span></span> | <span data-ttu-id="fa665-128">值</span><span class="sxs-lookup"><span data-stu-id="fa665-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa665-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa665-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fa665-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa665-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fa665-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa665-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fa665-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa665-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fa665-133">標頭</span><span class="sxs-lookup"><span data-stu-id="fa665-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa665-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fa665-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fa665-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa665-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa665-136"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa665-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa665-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fa665-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa665-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa665-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




