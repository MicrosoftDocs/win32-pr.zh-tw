---
description: 取得 \_ 錯誤記錄檔方法會抓取這個物件目前的錯誤記錄檔。
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'IAMSetErrorLog：： get_ErrorLog 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990170"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="28868-103">IAMSetErrorLog：：取得 \_ 錯誤記錄方法</span><span class="sxs-lookup"><span data-stu-id="28868-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="28868-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="28868-104">\[Deprecated.</span></span> <span data-ttu-id="28868-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="28868-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="28868-106">方法會抓取 `get_ErrorLog` 這個物件目前的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="28868-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="28868-107">語法</span><span class="sxs-lookup"><span data-stu-id="28868-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="28868-108">參數</span><span class="sxs-lookup"><span data-stu-id="28868-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28868-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="28868-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="28868-110">接收錯誤記錄檔之 [**IAMErrorLog**](iamerrorlog.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="28868-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="28868-111">如果時間軸沒有錯誤記錄檔，此值會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="28868-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28868-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="28868-112">Return value</span></span>

<span data-ttu-id="28868-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="28868-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28868-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28868-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28868-115">備註</span><span class="sxs-lookup"><span data-stu-id="28868-115">Remarks</span></span>

<span data-ttu-id="28868-116">如果 *pVal* 中傳回的值不是 **Null**，則 [**IAMErrorLog**](iamerrorlog.md) 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="28868-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="28868-117">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="28868-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="28868-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="28868-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="28868-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="28868-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="28868-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="28868-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28868-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="28868-121">Requirements</span></span>



| <span data-ttu-id="28868-122">需求</span><span class="sxs-lookup"><span data-stu-id="28868-122">Requirement</span></span> | <span data-ttu-id="28868-123">值</span><span class="sxs-lookup"><span data-stu-id="28868-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28868-124">標頭</span><span class="sxs-lookup"><span data-stu-id="28868-124">Header</span></span><br/>  | <dl> <span data-ttu-id="28868-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="28868-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="28868-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="28868-126">Library</span></span><br/> | <dl> <span data-ttu-id="28868-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28868-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28868-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28868-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28868-129">**IAMSetErrorLog 介面**</span><span class="sxs-lookup"><span data-stu-id="28868-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="28868-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="28868-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




