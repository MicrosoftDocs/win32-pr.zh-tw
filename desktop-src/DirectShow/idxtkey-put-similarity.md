---
description: Put \_ 相似性方法會指定變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey：:p ut_Similarity 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994140"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="b09fb-105">IDxtKey：:p ui \_ 相似性方法</span><span class="sxs-lookup"><span data-stu-id="b09fb-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="b09fb-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b09fb-106">\[Deprecated.</span></span> <span data-ttu-id="b09fb-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b09fb-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b09fb-108">`put_Similarity`方法會指定變成透明的色彩資料範圍。</span><span class="sxs-lookup"><span data-stu-id="b09fb-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="b09fb-109">在較高的值中，較大範圍的相似色彩是透明的。</span><span class="sxs-lookup"><span data-stu-id="b09fb-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="b09fb-110">只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b09fb-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09fb-111">語法</span><span class="sxs-lookup"><span data-stu-id="b09fb-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b09fb-112">參數</span><span class="sxs-lookup"><span data-stu-id="b09fb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b09fb-113">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b09fb-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b09fb-114">指定相似性值。</span><span class="sxs-lookup"><span data-stu-id="b09fb-114">Specifies the similarity value.</span></span> <span data-ttu-id="b09fb-115">有效範圍是從0到100。</span><span class="sxs-lookup"><span data-stu-id="b09fb-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b09fb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b09fb-116">Return value</span></span>

<span data-ttu-id="b09fb-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b09fb-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b09fb-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b09fb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b09fb-119">備註</span><span class="sxs-lookup"><span data-stu-id="b09fb-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b09fb-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b09fb-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b09fb-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b09fb-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b09fb-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b09fb-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b09fb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b09fb-123">Requirements</span></span>



| <span data-ttu-id="b09fb-124">需求</span><span class="sxs-lookup"><span data-stu-id="b09fb-124">Requirement</span></span> | <span data-ttu-id="b09fb-125">值</span><span class="sxs-lookup"><span data-stu-id="b09fb-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b09fb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b09fb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b09fb-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b09fb-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b09fb-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b09fb-128">Library</span></span><br/> | <dl> <span data-ttu-id="b09fb-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b09fb-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09fb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b09fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09fb-131">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="b09fb-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="b09fb-132">**IDxtKey：:p 的 ui \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="b09fb-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




