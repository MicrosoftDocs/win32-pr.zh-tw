---
description: Put \_ 錯誤記錄方法會指定物件的錯誤記錄檔。
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'IAMSetErrorLog：:p ut_ErrorLog 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981346"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="443a5-103">IAMSetErrorLog：:p 錯誤記錄檔 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="443a5-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="443a5-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="443a5-104">\[Deprecated.</span></span> <span data-ttu-id="443a5-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="443a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="443a5-106">`put_ErrorLog`方法會指定物件的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="443a5-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="443a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="443a5-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="443a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="443a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443a5-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="443a5-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443a5-110">錯誤記錄檔之 [**IAMErrorLog**](iamerrorlog.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="443a5-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443a5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="443a5-111">Return value</span></span>

<span data-ttu-id="443a5-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="443a5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="443a5-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="443a5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="443a5-114">備註</span><span class="sxs-lookup"><span data-stu-id="443a5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="443a5-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="443a5-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="443a5-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="443a5-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="443a5-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="443a5-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="443a5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="443a5-118">Requirements</span></span>



| <span data-ttu-id="443a5-119">需求</span><span class="sxs-lookup"><span data-stu-id="443a5-119">Requirement</span></span> | <span data-ttu-id="443a5-120">值</span><span class="sxs-lookup"><span data-stu-id="443a5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="443a5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="443a5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="443a5-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="443a5-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="443a5-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="443a5-123">Library</span></span><br/> | <dl> <span data-ttu-id="443a5-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="443a5-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443a5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="443a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443a5-126">**IAMSetErrorLog 介面**</span><span class="sxs-lookup"><span data-stu-id="443a5-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="443a5-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="443a5-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




