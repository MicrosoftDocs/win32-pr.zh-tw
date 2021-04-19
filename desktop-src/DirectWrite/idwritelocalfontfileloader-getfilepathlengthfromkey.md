---
title: IDWriteLocalFontFileLoader GetFilePathLengthFromKey 方法
description: 從字型檔案參考索引鍵取得絕對檔案路徑的長度。
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- GetFilePathLengthFromKey 方法直接寫入
- GetFilePathLengthFromKey 方法 Direct Write，IDWriteLocalFontFileLoader 介面
- IDWriteLocalFontFileLoader 介面 Direct Write，GetFilePathLengthFromKey 方法
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994991"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="578f6-106">IDWriteLocalFontFileLoader：： GetFilePathLengthFromKey 方法</span><span class="sxs-lookup"><span data-stu-id="578f6-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="578f6-107">從字型檔案參考索引鍵取得絕對檔案路徑的長度。</span><span class="sxs-lookup"><span data-stu-id="578f6-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="578f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="578f6-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="578f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="578f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578f6-110">*fontFileReferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="578f6-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578f6-111">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="578f6-111">Type: **const void\***</span></span>

<span data-ttu-id="578f6-112">字型檔案參考索引鍵，可在使用的字型載入器範圍內唯一識別本機字型檔案。</span><span class="sxs-lookup"><span data-stu-id="578f6-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="578f6-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="578f6-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="578f6-114">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="578f6-114">Type: **UINT32**</span></span>

<span data-ttu-id="578f6-115">字型檔案參考索引鍵的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="578f6-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="578f6-116">*filePathLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="578f6-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="578f6-117">類型： **UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="578f6-117">Type: **UINT32\***</span></span>

<span data-ttu-id="578f6-118">檔案路徑字串的長度，不包含終止的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="578f6-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578f6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="578f6-119">Return value</span></span>

<span data-ttu-id="578f6-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="578f6-120">Type: **HRESULT**</span></span>

<span data-ttu-id="578f6-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="578f6-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="578f6-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="578f6-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="578f6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="578f6-123">Requirements</span></span>



| <span data-ttu-id="578f6-124">需求</span><span class="sxs-lookup"><span data-stu-id="578f6-124">Requirement</span></span> | <span data-ttu-id="578f6-125">值</span><span class="sxs-lookup"><span data-stu-id="578f6-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="578f6-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="578f6-126">Library</span></span><br/> | <dl> <span data-ttu-id="578f6-127"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="578f6-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="578f6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="578f6-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="578f6-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="578f6-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="578f6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="578f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578f6-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="578f6-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





