---
description: GetGenID 方法會抓取物件所產生的識別碼。 識別碼是保留的數位;應用程式不應使用它。
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'IAMTimelineObj：： GetGenID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991152"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="5874a-104">IAMTimelineObj：： GetGenID 方法</span><span class="sxs-lookup"><span data-stu-id="5874a-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="5874a-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5874a-105">\[Deprecated.</span></span> <span data-ttu-id="5874a-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5874a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5874a-107">方法會抓取 `GetGenID` 物件所產生的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5874a-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="5874a-108">識別碼是保留的數位;應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="5874a-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="5874a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5874a-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5874a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5874a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5874a-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="5874a-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5874a-112">接收產生的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5874a-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5874a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5874a-113">Return value</span></span>

<span data-ttu-id="5874a-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5874a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5874a-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5874a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5874a-116">備註</span><span class="sxs-lookup"><span data-stu-id="5874a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5874a-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5874a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5874a-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5874a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5874a-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5874a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5874a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5874a-120">Requirements</span></span>



| <span data-ttu-id="5874a-121">需求</span><span class="sxs-lookup"><span data-stu-id="5874a-121">Requirement</span></span> | <span data-ttu-id="5874a-122">值</span><span class="sxs-lookup"><span data-stu-id="5874a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5874a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5874a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5874a-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5874a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5874a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5874a-125">Library</span></span><br/> | <dl> <span data-ttu-id="5874a-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5874a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5874a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5874a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5874a-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="5874a-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5874a-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5874a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




