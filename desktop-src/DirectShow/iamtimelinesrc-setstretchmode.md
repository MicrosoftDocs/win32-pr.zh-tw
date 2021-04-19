---
description: SetStretchMode 方法會設定延展模式。 如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'IAMTimelineSrc：： SetStretchMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998715"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="4cd9e-104">IAMTimelineSrc：： SetStretchMode 方法</span><span class="sxs-lookup"><span data-stu-id="4cd9e-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="4cd9e-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-105">\[Deprecated.</span></span> <span data-ttu-id="4cd9e-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4cd9e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cd9e-107">`SetStretchMode`方法會設定延展模式。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="4cd9e-108">如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd9e-109">語法</span><span class="sxs-lookup"><span data-stu-id="4cd9e-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="4cd9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4cd9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd9e-111">*nStretchMode*</span><span class="sxs-lookup"><span data-stu-id="4cd9e-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="4cd9e-112">指出目前延展模式的旗標。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="4cd9e-113">如需可能值的清單，請參閱 [**調整旗標**](resize-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd9e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cd9e-114">Return value</span></span>

<span data-ttu-id="4cd9e-115">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cd9e-116">備註</span><span class="sxs-lookup"><span data-stu-id="4cd9e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4cd9e-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cd9e-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4cd9e-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4cd9e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cd9e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cd9e-120">Requirements</span></span>



| <span data-ttu-id="4cd9e-121">需求</span><span class="sxs-lookup"><span data-stu-id="4cd9e-121">Requirement</span></span> | <span data-ttu-id="4cd9e-122">值</span><span class="sxs-lookup"><span data-stu-id="4cd9e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd9e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4cd9e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4cd9e-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4cd9e-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cd9e-125">Library</span></span><br/> | <dl> <span data-ttu-id="4cd9e-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cd9e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd9e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cd9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd9e-128">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="4cd9e-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4cd9e-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4cd9e-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




