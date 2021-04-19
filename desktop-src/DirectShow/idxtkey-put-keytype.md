---
description: Put \_ KeyType 方法會指定索引鍵的類型。
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'IDxtKey：:p ut_KeyType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978668"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="b3e81-103">IDxtKey：:p 的 ui \_ KeyType 方法</span><span class="sxs-lookup"><span data-stu-id="b3e81-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="b3e81-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b3e81-104">\[Deprecated.</span></span> <span data-ttu-id="b3e81-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b3e81-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b3e81-106">`put_KeyType`方法會指定索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="b3e81-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e81-107">語法</span><span class="sxs-lookup"><span data-stu-id="b3e81-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b3e81-108">參數</span><span class="sxs-lookup"><span data-stu-id="b3e81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e81-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3e81-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e81-110">指定金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="b3e81-110">Specifies the key type.</span></span> <span data-ttu-id="b3e81-111">此參數必須是下列其中一個列舉值。</span><span class="sxs-lookup"><span data-stu-id="b3e81-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="b3e81-112">值</span><span class="sxs-lookup"><span data-stu-id="b3e81-112">Value</span></span>             | <span data-ttu-id="b3e81-113">描述</span><span class="sxs-lookup"><span data-stu-id="b3e81-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b3e81-114">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="b3e81-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="b3e81-115">色度鍵。</span><span class="sxs-lookup"><span data-stu-id="b3e81-115">Chroma key.</span></span> <span data-ttu-id="b3e81-116"> (RGB 值的索引鍵。 ) </span><span class="sxs-lookup"><span data-stu-id="b3e81-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="b3e81-117">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="b3e81-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="b3e81-118">Nonred 鍵。</span><span class="sxs-lookup"><span data-stu-id="b3e81-118">Nonred key.</span></span> <span data-ttu-id="b3e81-119"> (使藍和綠區域透明。 ) </span><span class="sxs-lookup"><span data-stu-id="b3e81-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="b3e81-120">DXTKEY \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="b3e81-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="b3e81-121">亮度索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b3e81-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="b3e81-122">DXTKEY \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="b3e81-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="b3e81-123">依字母值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b3e81-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="b3e81-124">DXTKEY \_ 色調</span><span class="sxs-lookup"><span data-stu-id="b3e81-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="b3e81-125">按鍵（依色調）。</span><span class="sxs-lookup"><span data-stu-id="b3e81-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e81-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3e81-126">Return value</span></span>

<span data-ttu-id="b3e81-127">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b3e81-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3e81-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3e81-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e81-129">備註</span><span class="sxs-lookup"><span data-stu-id="b3e81-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b3e81-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b3e81-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b3e81-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b3e81-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b3e81-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b3e81-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3e81-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3e81-133">Requirements</span></span>



| <span data-ttu-id="b3e81-134">需求</span><span class="sxs-lookup"><span data-stu-id="b3e81-134">Requirement</span></span> | <span data-ttu-id="b3e81-135">值</span><span class="sxs-lookup"><span data-stu-id="b3e81-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e81-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b3e81-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b3e81-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e81-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b3e81-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3e81-138">Library</span></span><br/> | <dl> <span data-ttu-id="b3e81-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3e81-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e81-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3e81-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e81-141">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="b3e81-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




