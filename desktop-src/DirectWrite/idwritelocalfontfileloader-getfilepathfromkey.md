---
title: IDWriteLocalFontFileLoader GetFilePathFromKey 方法
description: 從字型檔案參考索引鍵取得絕對字型檔案路徑。
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- GetFilePathFromKey 方法直接寫入
- GetFilePathFromKey 方法 Direct Write，IDWriteLocalFontFileLoader 介面
- IDWriteLocalFontFileLoader 介面 Direct Write，GetFilePathFromKey 方法
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000840"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="e5215-106">IDWriteLocalFontFileLoader：： GetFilePathFromKey 方法</span><span class="sxs-lookup"><span data-stu-id="e5215-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="e5215-107">從字型檔案參考索引鍵取得絕對字型檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e5215-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5215-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5215-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e5215-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5215-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5215-110">*fontFileReferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5215-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5215-111">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="e5215-111">Type: **const void\***</span></span>

<span data-ttu-id="e5215-112">字型檔案參考索引鍵，可在使用的字型載入器範圍內唯一識別本機字型檔案。</span><span class="sxs-lookup"><span data-stu-id="e5215-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="e5215-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="e5215-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="e5215-114">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5215-114">Type: **UINT32**</span></span>

<span data-ttu-id="e5215-115">字型檔案參考索引鍵的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5215-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e5215-116">*filePath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e5215-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5215-117">類型： **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="e5215-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="e5215-118">接收本機檔案路徑的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="e5215-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="e5215-119">*filePathSize*</span><span class="sxs-lookup"><span data-stu-id="e5215-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="e5215-120">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5215-120">Type: **UINT32**</span></span>

<span data-ttu-id="e5215-121">檔案路徑字元陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="e5215-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5215-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5215-122">Return value</span></span>

<span data-ttu-id="e5215-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5215-123">Type: **HRESULT**</span></span>

<span data-ttu-id="e5215-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e5215-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5215-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e5215-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5215-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5215-126">Requirements</span></span>



| <span data-ttu-id="e5215-127">需求</span><span class="sxs-lookup"><span data-stu-id="e5215-127">Requirement</span></span> | <span data-ttu-id="e5215-128">值</span><span class="sxs-lookup"><span data-stu-id="e5215-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5215-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5215-129">Library</span></span><br/> | <dl> <span data-ttu-id="e5215-130"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5215-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5215-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e5215-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5215-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5215-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5215-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5215-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5215-134">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="e5215-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





