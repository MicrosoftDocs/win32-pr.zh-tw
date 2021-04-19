---
title: IDWriteLocalFontFileLoader GetLastWriteTimeFromKey 方法
description: 從字型檔案參考索引鍵取得檔案的上次寫入時間。
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- GetLastWriteTimeFromKey 方法直接寫入
- GetLastWriteTimeFromKey 方法 Direct Write，IDWriteLocalFontFileLoader 介面
- IDWriteLocalFontFileLoader 介面 Direct Write，GetLastWriteTimeFromKey 方法
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001910"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="314c9-106">IDWriteLocalFontFileLoader：： GetLastWriteTimeFromKey 方法</span><span class="sxs-lookup"><span data-stu-id="314c9-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="314c9-107">從字型檔案參考索引鍵取得檔案的上次寫入時間。</span><span class="sxs-lookup"><span data-stu-id="314c9-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="314c9-108">語法</span><span class="sxs-lookup"><span data-stu-id="314c9-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="314c9-109">參數</span><span class="sxs-lookup"><span data-stu-id="314c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314c9-110">*fontFileReferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="314c9-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314c9-111">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="314c9-111">Type: **const void\***</span></span>

<span data-ttu-id="314c9-112">字型檔案參考索引鍵，可在使用的字型載入器範圍內唯一識別本機字型檔案。</span><span class="sxs-lookup"><span data-stu-id="314c9-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="314c9-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="314c9-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="314c9-114">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="314c9-114">Type: **UINT32**</span></span>

<span data-ttu-id="314c9-115">字型檔案參考索引鍵的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="314c9-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="314c9-116">*lastWriteTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="314c9-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="314c9-117">類型： **FILETIME \***</span><span class="sxs-lookup"><span data-stu-id="314c9-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="314c9-118">上次修改字型檔案的時間。</span><span class="sxs-lookup"><span data-stu-id="314c9-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314c9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="314c9-119">Return value</span></span>

<span data-ttu-id="314c9-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="314c9-120">Type: **HRESULT**</span></span>

<span data-ttu-id="314c9-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="314c9-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="314c9-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="314c9-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="314c9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="314c9-123">Requirements</span></span>



| <span data-ttu-id="314c9-124">需求</span><span class="sxs-lookup"><span data-stu-id="314c9-124">Requirement</span></span> | <span data-ttu-id="314c9-125">值</span><span class="sxs-lookup"><span data-stu-id="314c9-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="314c9-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="314c9-126">Library</span></span><br/> | <dl> <span data-ttu-id="314c9-127"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="314c9-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="314c9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="314c9-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="314c9-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="314c9-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314c9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="314c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314c9-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="314c9-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





