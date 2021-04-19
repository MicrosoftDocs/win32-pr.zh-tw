---
description: 用來解壓縮編碼的資料。 這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。 從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader：:D ecompress 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982209"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="c9e21-105">ID3DX10DataLoader：:D ecompress 方法</span><span class="sxs-lookup"><span data-stu-id="c9e21-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="c9e21-106">用來解壓縮編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="c9e21-106">Used to decompress encoded data.</span></span> <span data-ttu-id="c9e21-107">這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。</span><span class="sxs-lookup"><span data-stu-id="c9e21-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="c9e21-108">從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="c9e21-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e21-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9e21-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="c9e21-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9e21-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e21-111">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9e21-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e21-112">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="c9e21-112">Type: **void\*\***</span></span>

<span data-ttu-id="c9e21-113">要解壓縮之原始資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c9e21-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="c9e21-114">*pcBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9e21-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e21-115">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9e21-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c9e21-116">PpData 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="c9e21-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e21-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9e21-117">Return value</span></span>

<span data-ttu-id="c9e21-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9e21-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9e21-119">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c9e21-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9e21-120">備註</span><span class="sxs-lookup"><span data-stu-id="c9e21-120">Remarks</span></span>

<span data-ttu-id="c9e21-121">您可以繼承 [**ID3DX10DataLoader 介面**](id3dx10dataloader.md)，也可以重新定義其成員。</span><span class="sxs-lookup"><span data-stu-id="c9e21-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="c9e21-122">您可以重新定義解壓縮，以支援您自己的自訂檔案格式。</span><span class="sxs-lookup"><span data-stu-id="c9e21-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e21-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9e21-123">Requirements</span></span>



| <span data-ttu-id="c9e21-124">需求</span><span class="sxs-lookup"><span data-stu-id="c9e21-124">Requirement</span></span> | <span data-ttu-id="c9e21-125">值</span><span class="sxs-lookup"><span data-stu-id="c9e21-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e21-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c9e21-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c9e21-127"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9e21-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9e21-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9e21-128">Library</span></span><br/> | <dl> <span data-ttu-id="c9e21-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9e21-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e21-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9e21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e21-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="c9e21-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="c9e21-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c9e21-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
