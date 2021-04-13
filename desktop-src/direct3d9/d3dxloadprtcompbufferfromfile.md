---
description: 載入至記憶體中已壓縮的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: 'D3DXLoadPRTCompBufferFromFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323303"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="3aed9-103">D3DXLoadPRTCompBufferFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="3aed9-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="3aed9-104">載入至記憶體中已壓縮的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3aed9-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aed9-105">語法</span><span class="sxs-lookup"><span data-stu-id="3aed9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3aed9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3aed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aed9-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3aed9-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aed9-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aed9-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aed9-109">要從中載入壓縮緩衝區資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3aed9-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="3aed9-110">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3aed9-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aed9-111">類型： **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3aed9-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="3aed9-112">輸出 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="3aed9-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aed9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3aed9-113">Return value</span></span>

<span data-ttu-id="3aed9-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3aed9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3aed9-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3aed9-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3aed9-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3aed9-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aed9-117">備註</span><span class="sxs-lookup"><span data-stu-id="3aed9-117">Remarks</span></span>

<span data-ttu-id="3aed9-118">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="3aed9-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3aed9-119">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadPRTCompBufferFromFileW。</span><span class="sxs-lookup"><span data-stu-id="3aed9-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="3aed9-120">否則，函式呼叫會解析為 D3DXLoadPRTCompBufferFromFileA。</span><span class="sxs-lookup"><span data-stu-id="3aed9-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aed9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3aed9-121">Requirements</span></span>



| <span data-ttu-id="3aed9-122">需求</span><span class="sxs-lookup"><span data-stu-id="3aed9-122">Requirement</span></span> | <span data-ttu-id="3aed9-123">值</span><span class="sxs-lookup"><span data-stu-id="3aed9-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aed9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3aed9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3aed9-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3aed9-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3aed9-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3aed9-126">Library</span></span><br/> | <dl> <span data-ttu-id="3aed9-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aed9-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3aed9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aed9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aed9-129">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="3aed9-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
