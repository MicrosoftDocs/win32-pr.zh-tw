---
description: GetStretchMode 方法會抓取延展模式。 如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'IAMTimelineSrc：： GetStretchMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980211"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="ab9d7-104">IAMTimelineSrc：： GetStretchMode 方法</span><span class="sxs-lookup"><span data-stu-id="ab9d7-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="ab9d7-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-105">\[Deprecated.</span></span> <span data-ttu-id="ab9d7-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ab9d7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ab9d7-107">方法會抓取 `GetStretchMode` 延展模式。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="ab9d7-108">如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9d7-109">語法</span><span class="sxs-lookup"><span data-stu-id="ab9d7-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="ab9d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab9d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9d7-111">*pnStretchMode*</span><span class="sxs-lookup"><span data-stu-id="ab9d7-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="ab9d7-112">接收旗標，指出目前的延展模式。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="ab9d7-113">如需可能值的清單，請參閱 [**調整旗標**](resize-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9d7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab9d7-114">Return value</span></span>

<span data-ttu-id="ab9d7-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab9d7-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9d7-117">備註</span><span class="sxs-lookup"><span data-stu-id="ab9d7-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ab9d7-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ab9d7-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ab9d7-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ab9d7-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab9d7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab9d7-121">Requirements</span></span>



| <span data-ttu-id="ab9d7-122">需求</span><span class="sxs-lookup"><span data-stu-id="ab9d7-122">Requirement</span></span> | <span data-ttu-id="ab9d7-123">值</span><span class="sxs-lookup"><span data-stu-id="ab9d7-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9d7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ab9d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ab9d7-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9d7-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab9d7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab9d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="ab9d7-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab9d7-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab9d7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab9d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9d7-129">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="ab9d7-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ab9d7-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ab9d7-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




