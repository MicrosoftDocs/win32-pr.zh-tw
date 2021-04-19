---
description: GetTimelineType 方法會抓取物件的型別。
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'IAMTimelineObj：： GetTimelineType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982257"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="cea86-103">IAMTimelineObj：： GetTimelineType 方法</span><span class="sxs-lookup"><span data-stu-id="cea86-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="cea86-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="cea86-104">\[Deprecated.</span></span> <span data-ttu-id="cea86-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="cea86-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cea86-106">方法會抓取 `GetTimelineType` 物件的型別。</span><span class="sxs-lookup"><span data-stu-id="cea86-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea86-107">語法</span><span class="sxs-lookup"><span data-stu-id="cea86-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cea86-108">參數</span><span class="sxs-lookup"><span data-stu-id="cea86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea86-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="cea86-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="cea86-110">接收 [**時間軸 \_ 主要 \_ 型**](timeline-major-type.md) 別列舉型別的成員，指出物件的型別。</span><span class="sxs-lookup"><span data-stu-id="cea86-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea86-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cea86-111">Return value</span></span>

<span data-ttu-id="cea86-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cea86-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cea86-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cea86-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea86-114">備註</span><span class="sxs-lookup"><span data-stu-id="cea86-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cea86-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="cea86-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cea86-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cea86-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cea86-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="cea86-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cea86-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cea86-118">Requirements</span></span>



| <span data-ttu-id="cea86-119">需求</span><span class="sxs-lookup"><span data-stu-id="cea86-119">Requirement</span></span> | <span data-ttu-id="cea86-120">值</span><span class="sxs-lookup"><span data-stu-id="cea86-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea86-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cea86-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cea86-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cea86-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cea86-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cea86-123">Library</span></span><br/> | <dl> <span data-ttu-id="cea86-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea86-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea86-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cea86-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea86-126">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="cea86-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="cea86-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="cea86-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




