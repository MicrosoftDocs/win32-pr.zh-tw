---
description: SaveToBlob 方法會將屬性資料儲存至保存格式。
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter：： SaveToBlob 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989868"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="b86ad-103">IPropertySetter：： SaveToBlob 方法</span><span class="sxs-lookup"><span data-stu-id="b86ad-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="b86ad-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b86ad-104">\[Deprecated.</span></span> <span data-ttu-id="b86ad-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b86ad-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b86ad-106">方法會將 `SaveToBlob` 屬性資料儲存至保存格式。</span><span class="sxs-lookup"><span data-stu-id="b86ad-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="b86ad-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="b86ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="b86ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86ad-109">*pcSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b86ad-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ad-110">接收資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b86ad-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b86ad-111">*ppb* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b86ad-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ad-112">接收接收資料之位元組陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b86ad-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86ad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b86ad-113">Return value</span></span>

<span data-ttu-id="b86ad-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b86ad-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b86ad-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b86ad-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86ad-116">備註</span><span class="sxs-lookup"><span data-stu-id="b86ad-116">Remarks</span></span>

<span data-ttu-id="b86ad-117">方法會配置位元組陣列的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b86ad-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="b86ad-118">呼叫端必須使用 **CoTaskMemFree** 函數釋放它。</span><span class="sxs-lookup"><span data-stu-id="b86ad-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="b86ad-119">所有屬性名稱和值的長度都會截斷為40個字元。</span><span class="sxs-lookup"><span data-stu-id="b86ad-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="b86ad-120">基於這個理由，XML 是慣用的持續性格式。</span><span class="sxs-lookup"><span data-stu-id="b86ad-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="b86ad-121">請參閱 [**IXml2Dex 介面**](ixml2dex.md)。</span><span class="sxs-lookup"><span data-stu-id="b86ad-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="b86ad-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b86ad-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b86ad-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b86ad-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b86ad-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b86ad-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b86ad-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b86ad-125">Requirements</span></span>



| <span data-ttu-id="b86ad-126">需求</span><span class="sxs-lookup"><span data-stu-id="b86ad-126">Requirement</span></span> | <span data-ttu-id="b86ad-127">值</span><span class="sxs-lookup"><span data-stu-id="b86ad-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b86ad-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b86ad-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b86ad-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b86ad-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b86ad-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="b86ad-130">Library</span></span><br/> | <dl> <span data-ttu-id="b86ad-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86ad-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86ad-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b86ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86ad-133">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="b86ad-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="b86ad-134">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b86ad-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




