---
title: 'ID3DX11DataLoader 解壓縮方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 解壓縮編碼的資料。
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- 解壓縮方法 Direct3D 11
- 解壓縮方法 Direct3D 11，ID3DX11DataLoader 介面
- ID3DX11DataLoader 介面 Direct3D 11，解壓縮方法
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946256"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="cef9f-107">ID3DX11DataLoader：:D ecompress 方法</span><span class="sxs-lookup"><span data-stu-id="cef9f-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="cef9f-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cef9f-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="cef9f-109">解壓縮編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="cef9f-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef9f-110">語法</span><span class="sxs-lookup"><span data-stu-id="cef9f-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="cef9f-111">參數</span><span class="sxs-lookup"><span data-stu-id="cef9f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef9f-112">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cef9f-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cef9f-113">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="cef9f-113">Type: **void\*\***</span></span>

<span data-ttu-id="cef9f-114">要解壓縮之原始資料的指標。</span><span class="sxs-lookup"><span data-stu-id="cef9f-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="cef9f-115">*pcBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cef9f-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cef9f-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="cef9f-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cef9f-117">PpData 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="cef9f-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef9f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cef9f-118">Return value</span></span>

<span data-ttu-id="cef9f-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cef9f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cef9f-120">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cef9f-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cef9f-121">備註</span><span class="sxs-lookup"><span data-stu-id="cef9f-121">Remarks</span></span>

<span data-ttu-id="cef9f-122">使用這個方法可從檔案系統（例如 ZIP 檔案）載入資源。</span><span class="sxs-lookup"><span data-stu-id="cef9f-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="cef9f-123">從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="cef9f-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="cef9f-124">您可以繼承 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)，並重新定義其成員以支援自訂檔案格式。</span><span class="sxs-lookup"><span data-stu-id="cef9f-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef9f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cef9f-125">Requirements</span></span>



| <span data-ttu-id="cef9f-126">需求</span><span class="sxs-lookup"><span data-stu-id="cef9f-126">Requirement</span></span> | <span data-ttu-id="cef9f-127">值</span><span class="sxs-lookup"><span data-stu-id="cef9f-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cef9f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cef9f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cef9f-129"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="cef9f-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="cef9f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="cef9f-130">Library</span></span><br/> | <dl> <span data-ttu-id="cef9f-131"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cef9f-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cef9f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cef9f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef9f-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="cef9f-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="cef9f-134">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="cef9f-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

