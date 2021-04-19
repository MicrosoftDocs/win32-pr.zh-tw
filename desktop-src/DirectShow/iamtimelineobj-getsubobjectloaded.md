---
description: GetSubObjectLoaded 方法會判斷是否已設定子物件指標。
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'IAMTimelineObj：： GetSubObjectLoaded 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977657"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="15462-103">IAMTimelineObj：： GetSubObjectLoaded 方法</span><span class="sxs-lookup"><span data-stu-id="15462-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="15462-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="15462-104">\[Deprecated.</span></span> <span data-ttu-id="15462-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="15462-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15462-106">`GetSubObjectLoaded`方法會判斷是否已設定子物件指標。</span><span class="sxs-lookup"><span data-stu-id="15462-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="15462-107">語法</span><span class="sxs-lookup"><span data-stu-id="15462-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="15462-108">參數</span><span class="sxs-lookup"><span data-stu-id="15462-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15462-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="15462-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="15462-110">接收布林值。</span><span class="sxs-lookup"><span data-stu-id="15462-110">Receives a Boolean value.</span></span> <span data-ttu-id="15462-111">如果值為 **TRUE**，表示已設定子物件指標。</span><span class="sxs-lookup"><span data-stu-id="15462-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="15462-112">如果 **為 FALSE**，則表示指標尚未設定。</span><span class="sxs-lookup"><span data-stu-id="15462-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15462-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15462-113">Return value</span></span>

<span data-ttu-id="15462-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="15462-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15462-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="15462-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15462-116">備註</span><span class="sxs-lookup"><span data-stu-id="15462-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="15462-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="15462-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="15462-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="15462-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="15462-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="15462-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15462-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="15462-120">Requirements</span></span>



| <span data-ttu-id="15462-121">需求</span><span class="sxs-lookup"><span data-stu-id="15462-121">Requirement</span></span> | <span data-ttu-id="15462-122">值</span><span class="sxs-lookup"><span data-stu-id="15462-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15462-123">標頭</span><span class="sxs-lookup"><span data-stu-id="15462-123">Header</span></span><br/>  | <dl> <span data-ttu-id="15462-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="15462-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="15462-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="15462-125">Library</span></span><br/> | <dl> <span data-ttu-id="15462-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="15462-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15462-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15462-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15462-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="15462-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="15462-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="15462-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




