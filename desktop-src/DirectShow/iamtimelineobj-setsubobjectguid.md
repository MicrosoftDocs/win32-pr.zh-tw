---
description: SetSubObjectGUID 方法會指定與這個物件相關聯的子物件的 GUID。
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'IAMTimelineObj：： SetSubObjectGUID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976175"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="11951-103">IAMTimelineObj：： SetSubObjectGUID 方法</span><span class="sxs-lookup"><span data-stu-id="11951-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="11951-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="11951-104">\[Deprecated.</span></span> <span data-ttu-id="11951-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="11951-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="11951-106">`SetSubObjectGUID`方法會指定與這個物件相關聯之子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="11951-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="11951-107">語法</span><span class="sxs-lookup"><span data-stu-id="11951-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="11951-108">參數</span><span class="sxs-lookup"><span data-stu-id="11951-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11951-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="11951-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="11951-110">子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="11951-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11951-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11951-111">Return value</span></span>

<span data-ttu-id="11951-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="11951-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11951-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="11951-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11951-114">備註</span><span class="sxs-lookup"><span data-stu-id="11951-114">Remarks</span></span>

<span data-ttu-id="11951-115">轉譯引擎會視需要建立子物件的實例。</span><span class="sxs-lookup"><span data-stu-id="11951-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="11951-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="11951-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="11951-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="11951-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="11951-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="11951-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11951-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="11951-119">Requirements</span></span>



| <span data-ttu-id="11951-120">需求</span><span class="sxs-lookup"><span data-stu-id="11951-120">Requirement</span></span> | <span data-ttu-id="11951-121">值</span><span class="sxs-lookup"><span data-stu-id="11951-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11951-122">標頭</span><span class="sxs-lookup"><span data-stu-id="11951-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11951-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="11951-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="11951-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="11951-124">Library</span></span><br/> | <dl> <span data-ttu-id="11951-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="11951-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11951-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11951-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11951-127">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="11951-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="11951-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="11951-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




