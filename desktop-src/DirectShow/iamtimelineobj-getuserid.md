---
description: GetUserID 方法會抓取物件的應用程式定義識別碼。
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: 'IAMTimelineObj：： GetUserID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985930"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="6a596-103">IAMTimelineObj：： GetUserID 方法</span><span class="sxs-lookup"><span data-stu-id="6a596-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="6a596-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6a596-104">\[Deprecated.</span></span> <span data-ttu-id="6a596-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6a596-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6a596-106">方法會抓取 `GetUserID` 物件的應用程式定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a596-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a596-107">語法</span><span class="sxs-lookup"><span data-stu-id="6a596-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6a596-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a596-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a596-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="6a596-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6a596-110">接收應用程式定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a596-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a596-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a596-111">Return value</span></span>

<span data-ttu-id="6a596-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6a596-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a596-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a596-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a596-114">備註</span><span class="sxs-lookup"><span data-stu-id="6a596-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a596-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6a596-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6a596-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6a596-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6a596-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6a596-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a596-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a596-118">Requirements</span></span>



| <span data-ttu-id="6a596-119">需求</span><span class="sxs-lookup"><span data-stu-id="6a596-119">Requirement</span></span> | <span data-ttu-id="6a596-120">值</span><span class="sxs-lookup"><span data-stu-id="6a596-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a596-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6a596-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6a596-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a596-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a596-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a596-123">Library</span></span><br/> | <dl> <span data-ttu-id="6a596-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a596-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a596-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a596-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a596-126">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="6a596-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6a596-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6a596-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




