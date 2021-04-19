---
description: 取得 \_ 相似性方法會抓取變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'IDxtKey：： get_Similarity 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000759"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="fcc4f-105">IDxtKey：：取得 \_ 相似性方法</span><span class="sxs-lookup"><span data-stu-id="fcc4f-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="fcc4f-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-106">\[Deprecated.</span></span> <span data-ttu-id="fcc4f-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fcc4f-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fcc4f-108">`get_Similarity`方法會抓取變成透明的色彩資料範圍。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="fcc4f-109">在較高的值中，較大範圍的相似色彩是透明的。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="fcc4f-110">只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc4f-111">語法</span><span class="sxs-lookup"><span data-stu-id="fcc4f-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fcc4f-112">參數</span><span class="sxs-lookup"><span data-stu-id="fcc4f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc4f-113">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fcc4f-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc4f-114">接收相似性值。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc4f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcc4f-115">Return value</span></span>

<span data-ttu-id="fcc4f-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fcc4f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc4f-118">備註</span><span class="sxs-lookup"><span data-stu-id="fcc4f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fcc4f-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fcc4f-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fcc4f-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fcc4f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fcc4f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcc4f-122">Requirements</span></span>



| <span data-ttu-id="fcc4f-123">需求</span><span class="sxs-lookup"><span data-stu-id="fcc4f-123">Requirement</span></span> | <span data-ttu-id="fcc4f-124">值</span><span class="sxs-lookup"><span data-stu-id="fcc4f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc4f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fcc4f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fcc4f-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fcc4f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fcc4f-127">Library</span></span><br/> | <dl> <span data-ttu-id="fcc4f-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcc4f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc4f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcc4f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc4f-130">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="fcc4f-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="fcc4f-131">**IDxtKey：：取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="fcc4f-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




