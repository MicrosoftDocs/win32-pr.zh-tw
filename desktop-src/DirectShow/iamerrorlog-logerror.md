---
description: LogError 方法會記錄錯誤。 應用程式不需要呼叫此方法。 它會在內部呼叫，以回應呈現錯誤。
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog：： LogError 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993488"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="7ad86-105">IAMErrorLog：： LogError 方法</span><span class="sxs-lookup"><span data-stu-id="7ad86-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="7ad86-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7ad86-106">\[Deprecated.</span></span> <span data-ttu-id="7ad86-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7ad86-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ad86-108">**LogError** 方法會記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ad86-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="7ad86-109">應用程式不需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="7ad86-109">Applications do not need to call this method.</span></span> <span data-ttu-id="7ad86-110">它會在內部呼叫，以回應呈現錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ad86-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad86-111">語法</span><span class="sxs-lookup"><span data-stu-id="7ad86-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ad86-112">參數</span><span class="sxs-lookup"><span data-stu-id="7ad86-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad86-113">*嚴重性*</span><span class="sxs-lookup"><span data-stu-id="7ad86-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad86-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="7ad86-114">Reserved.</span></span> <span data-ttu-id="7ad86-115">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="7ad86-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="7ad86-116">*ErrorString*</span><span class="sxs-lookup"><span data-stu-id="7ad86-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad86-117">包含錯誤文字的字串值。</span><span class="sxs-lookup"><span data-stu-id="7ad86-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="7ad86-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="7ad86-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad86-119">錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7ad86-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="7ad86-120">*hresult*</span><span class="sxs-lookup"><span data-stu-id="7ad86-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad86-121">造成錯誤的方法呼叫所傳回的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="7ad86-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="7ad86-122">*pExtraInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ad86-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad86-123">VARIANT 的指標，其中包含有關錯誤的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7ad86-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad86-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ad86-124">Return value</span></span>

<span data-ttu-id="7ad86-125">傳回 *hresult* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="7ad86-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad86-126">備註</span><span class="sxs-lookup"><span data-stu-id="7ad86-126">Remarks</span></span>

<span data-ttu-id="7ad86-127">在這個方法中，請勿釋放 *pExtraInfo* 所指向的 **變異**。</span><span class="sxs-lookup"><span data-stu-id="7ad86-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="7ad86-128">此外，此 **變數** 會在方法傳回之後變成無效，因此請勿稍後再參考。</span><span class="sxs-lookup"><span data-stu-id="7ad86-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="7ad86-129">執行此方法以儘快傳回。</span><span class="sxs-lookup"><span data-stu-id="7ad86-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="7ad86-130">請勿從這個可能會封鎖程式執行的方法內部進行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="7ad86-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="7ad86-131">例如，請勿呼叫傳送視窗訊息、封鎖事件的函式，否則可能會封鎖執行。</span><span class="sxs-lookup"><span data-stu-id="7ad86-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="7ad86-132">這樣做可能會導致電腦停止回應。</span><span class="sxs-lookup"><span data-stu-id="7ad86-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="7ad86-133">如需 DES 定義的錯誤清單，以及 *pExtraInfo* 所指向之 **變異** 的意義和資料類型，請參閱轉譯 [錯誤](rendering-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="7ad86-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="7ad86-134">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7ad86-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ad86-135">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7ad86-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ad86-136">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7ad86-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ad86-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ad86-137">Requirements</span></span>



| <span data-ttu-id="7ad86-138">需求</span><span class="sxs-lookup"><span data-stu-id="7ad86-138">Requirement</span></span> | <span data-ttu-id="7ad86-139">值</span><span class="sxs-lookup"><span data-stu-id="7ad86-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad86-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7ad86-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7ad86-141"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad86-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ad86-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ad86-142">Library</span></span><br/> | <dl> <span data-ttu-id="7ad86-143"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad86-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad86-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ad86-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad86-145">**IAMErrorLog 介面**</span><span class="sxs-lookup"><span data-stu-id="7ad86-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="7ad86-146">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="7ad86-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




