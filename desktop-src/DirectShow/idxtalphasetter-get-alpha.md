---
description: Get \_ Alpha 方法會抓取整個影像的 Alpha 值。
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'IDxtAlphaSetter：： get_Alpha 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994691"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="5a7b9-103">IDxtAlphaSetter：： get \_ Alpha 方法</span><span class="sxs-lookup"><span data-stu-id="5a7b9-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="5a7b9-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-104">\[Deprecated.</span></span> <span data-ttu-id="5a7b9-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5a7b9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a7b9-106">方法會抓取 `get_Alpha` 整個影像的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a7b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a7b9-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="5a7b9-108">參數</span><span class="sxs-lookup"><span data-stu-id="5a7b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a7b9-109">*pAlpha* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5a7b9-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7b9-110">接收 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-110">Receives the alpha value.</span></span> <span data-ttu-id="5a7b9-111">此 Alpha 值會套用至整個目標影像。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="5a7b9-112">負數值表示未設定 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a7b9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a7b9-113">Return value</span></span>

<span data-ttu-id="5a7b9-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5a7b9-115">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-115">Possible values include the following.</span></span>



| <span data-ttu-id="5a7b9-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5a7b9-116">Return code</span></span>                                                                               | <span data-ttu-id="5a7b9-117">Description</span><span class="sxs-lookup"><span data-stu-id="5a7b9-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="5a7b9-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5a7b9-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5a7b9-119">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="5a7b9-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="5a7b9-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5a7b9-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5a7b9-121">Success</span><span class="sxs-lookup"><span data-stu-id="5a7b9-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="5a7b9-122">備註</span><span class="sxs-lookup"><span data-stu-id="5a7b9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a7b9-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a7b9-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a7b9-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5a7b9-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a7b9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a7b9-126">Requirements</span></span>



| <span data-ttu-id="5a7b9-127">需求</span><span class="sxs-lookup"><span data-stu-id="5a7b9-127">Requirement</span></span> | <span data-ttu-id="5a7b9-128">值</span><span class="sxs-lookup"><span data-stu-id="5a7b9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7b9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5a7b9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5a7b9-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a7b9-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a7b9-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a7b9-131">Library</span></span><br/> | <dl> <span data-ttu-id="5a7b9-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a7b9-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a7b9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a7b9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7b9-134">**IDxtAlphaSetter 介面**</span><span class="sxs-lookup"><span data-stu-id="5a7b9-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




