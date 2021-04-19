---
description: SetUserData 方法會設定應用程式定義的持續性資料。
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'IAMTimelineObj：： SetUserData 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993452"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="d3df6-103">IAMTimelineObj：： SetUserData 方法</span><span class="sxs-lookup"><span data-stu-id="d3df6-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="d3df6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d3df6-104">\[Deprecated.</span></span> <span data-ttu-id="d3df6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d3df6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d3df6-106">`SetUserData`方法會設定應用程式定義的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="d3df6-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3df6-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3df6-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="d3df6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3df6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3df6-109">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="d3df6-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d3df6-110">包含資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d3df6-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="d3df6-111">*大小*</span><span class="sxs-lookup"><span data-stu-id="d3df6-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="d3df6-112">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d3df6-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3df6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3df6-113">Return value</span></span>

<span data-ttu-id="d3df6-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d3df6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3df6-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d3df6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3df6-116">備註</span><span class="sxs-lookup"><span data-stu-id="d3df6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3df6-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d3df6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d3df6-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d3df6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d3df6-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d3df6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3df6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3df6-120">Requirements</span></span>



| <span data-ttu-id="d3df6-121">需求</span><span class="sxs-lookup"><span data-stu-id="d3df6-121">Requirement</span></span> | <span data-ttu-id="d3df6-122">值</span><span class="sxs-lookup"><span data-stu-id="d3df6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3df6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d3df6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d3df6-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3df6-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d3df6-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3df6-125">Library</span></span><br/> | <dl> <span data-ttu-id="d3df6-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3df6-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3df6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3df6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3df6-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="d3df6-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d3df6-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d3df6-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




