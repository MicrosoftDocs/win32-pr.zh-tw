---
description: LoadFromBlob 方法會從持續性格式載入屬性資料。
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'IPropertySetter：： LoadFromBlob 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977628"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="6537c-103">IPropertySetter：： LoadFromBlob 方法</span><span class="sxs-lookup"><span data-stu-id="6537c-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="6537c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6537c-104">\[Deprecated.</span></span> <span data-ttu-id="6537c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6537c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6537c-106">`LoadFromBlob`方法會從持續性格式載入屬性資料。</span><span class="sxs-lookup"><span data-stu-id="6537c-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6537c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6537c-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="6537c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6537c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6537c-109">*cSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6537c-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6537c-110">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6537c-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6537c-111">*pb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6537c-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6537c-112">包含資料之位元組陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="6537c-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6537c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6537c-113">Return value</span></span>

<span data-ttu-id="6537c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6537c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6537c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6537c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6537c-116">備註</span><span class="sxs-lookup"><span data-stu-id="6537c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6537c-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6537c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6537c-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6537c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6537c-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6537c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6537c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6537c-120">Requirements</span></span>



| <span data-ttu-id="6537c-121">需求</span><span class="sxs-lookup"><span data-stu-id="6537c-121">Requirement</span></span> | <span data-ttu-id="6537c-122">值</span><span class="sxs-lookup"><span data-stu-id="6537c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6537c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6537c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6537c-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6537c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6537c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6537c-125">Library</span></span><br/> | <dl> <span data-ttu-id="6537c-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6537c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6537c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6537c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6537c-128">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="6537c-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="6537c-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6537c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




