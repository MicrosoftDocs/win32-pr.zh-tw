---
description: SetMediaLength2 方法會指定原始程式檔的持續時間。 這個方法相當於 IAMTimelineSrc：： SetMediaLength，但會接受 REFTIME 值。
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'IAMTimelineSrc：： SetMediaLength2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997017"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="87587-104">IAMTimelineSrc：： SetMediaLength2 方法</span><span class="sxs-lookup"><span data-stu-id="87587-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="87587-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="87587-105">\[Deprecated.</span></span> <span data-ttu-id="87587-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="87587-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="87587-107">方法會指定原始程式檔的 `SetMediaLength2` 持續時間。</span><span class="sxs-lookup"><span data-stu-id="87587-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="87587-108">這個方法相當於 [**IAMTimelineSrc：： SetMediaLength**](iamtimelinesrc-setmedialength.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="87587-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="87587-109">語法</span><span class="sxs-lookup"><span data-stu-id="87587-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="87587-110">參數</span><span class="sxs-lookup"><span data-stu-id="87587-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87587-111">*長度*</span><span class="sxs-lookup"><span data-stu-id="87587-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="87587-112">媒體長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="87587-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87587-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="87587-113">Return value</span></span>

<span data-ttu-id="87587-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="87587-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87587-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="87587-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87587-116">備註</span><span class="sxs-lookup"><span data-stu-id="87587-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87587-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="87587-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="87587-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="87587-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="87587-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="87587-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87587-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="87587-120">Requirements</span></span>



| <span data-ttu-id="87587-121">需求</span><span class="sxs-lookup"><span data-stu-id="87587-121">Requirement</span></span> | <span data-ttu-id="87587-122">值</span><span class="sxs-lookup"><span data-stu-id="87587-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87587-123">標頭</span><span class="sxs-lookup"><span data-stu-id="87587-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87587-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="87587-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="87587-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="87587-125">Library</span></span><br/> | <dl> <span data-ttu-id="87587-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87587-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87587-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87587-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87587-128">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="87587-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="87587-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="87587-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




