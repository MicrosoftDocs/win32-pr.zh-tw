---
description: 取得 KeyType 方法會抓取索引 \_ 鍵的類型。
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'IDxtKey：： get_KeyType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998606"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="cb19d-103">IDxtKey：：取得 \_ KeyType 方法</span><span class="sxs-lookup"><span data-stu-id="cb19d-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="cb19d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="cb19d-104">\[Deprecated.</span></span> <span data-ttu-id="cb19d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="cb19d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb19d-106">方法會抓取索引 `get_KeyType` 鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="cb19d-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb19d-107">語法</span><span class="sxs-lookup"><span data-stu-id="cb19d-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cb19d-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb19d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb19d-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="cb19d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cb19d-110">接收下列其中一個列舉值。</span><span class="sxs-lookup"><span data-stu-id="cb19d-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="cb19d-111">值</span><span class="sxs-lookup"><span data-stu-id="cb19d-111">Value</span></span>             | <span data-ttu-id="cb19d-112">描述</span><span class="sxs-lookup"><span data-stu-id="cb19d-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="cb19d-113">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="cb19d-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="cb19d-114">色度鍵。</span><span class="sxs-lookup"><span data-stu-id="cb19d-114">Chroma key.</span></span> <span data-ttu-id="cb19d-115"> (RGB 值的索引鍵。 ) </span><span class="sxs-lookup"><span data-stu-id="cb19d-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="cb19d-116">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="cb19d-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="cb19d-117">Nonred 鍵。</span><span class="sxs-lookup"><span data-stu-id="cb19d-117">Nonred key.</span></span> <span data-ttu-id="cb19d-118"> (使藍和綠區域透明。 ) </span><span class="sxs-lookup"><span data-stu-id="cb19d-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="cb19d-119">DXTKEY \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="cb19d-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="cb19d-120">亮度索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cb19d-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="cb19d-121">DXTKEY \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="cb19d-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="cb19d-122">依字母值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cb19d-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="cb19d-123">DXTKEY \_ 色調</span><span class="sxs-lookup"><span data-stu-id="cb19d-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="cb19d-124">按鍵（依色調）。</span><span class="sxs-lookup"><span data-stu-id="cb19d-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb19d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb19d-125">Return value</span></span>

<span data-ttu-id="cb19d-126">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cb19d-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb19d-127">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cb19d-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb19d-128">備註</span><span class="sxs-lookup"><span data-stu-id="cb19d-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb19d-129">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="cb19d-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb19d-130">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cb19d-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb19d-131">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="cb19d-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb19d-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb19d-132">Requirements</span></span>



| <span data-ttu-id="cb19d-133">需求</span><span class="sxs-lookup"><span data-stu-id="cb19d-133">Requirement</span></span> | <span data-ttu-id="cb19d-134">值</span><span class="sxs-lookup"><span data-stu-id="cb19d-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb19d-135">標頭</span><span class="sxs-lookup"><span data-stu-id="cb19d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="cb19d-136"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb19d-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb19d-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb19d-137">Library</span></span><br/> | <dl> <span data-ttu-id="cb19d-138"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb19d-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb19d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb19d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb19d-140">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="cb19d-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




