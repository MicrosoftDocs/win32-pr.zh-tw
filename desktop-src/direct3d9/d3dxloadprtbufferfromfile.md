---
description: 載入至記憶體中的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: 'D3DXLoadPRTBufferFromFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322667"
---
# <a name="d3dxloadprtbufferfromfile-function"></a><span data-ttu-id="8a0f5-103">D3DXLoadPRTBufferFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="8a0f5-103">D3DXLoadPRTBufferFromFile function</span></span>

<span data-ttu-id="8a0f5-104">載入至記憶體中的預先計算 radiance 傳輸 (PRT 已儲存至磁片的) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-104">Loads into memory a precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a0f5-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8a0f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a0f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0f5-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a0f5-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0f5-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a0f5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a0f5-109">要從中載入緩衝區資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-109">Name of the file from which to load the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="8a0f5-110">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8a0f5-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0f5-111">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a0f5-111">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="8a0f5-112">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-112">Address of a pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0f5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a0f5-113">Return value</span></span>

<span data-ttu-id="8a0f5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a0f5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a0f5-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a0f5-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a0f5-117">備註</span><span class="sxs-lookup"><span data-stu-id="8a0f5-117">Remarks</span></span>

<span data-ttu-id="8a0f5-118">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8a0f5-119">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadPRTBufferFromFileW。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-119">If Unicode is defined, the function call resolves to D3DXLoadPRTBufferFromFileW.</span></span> <span data-ttu-id="8a0f5-120">否則，函式呼叫會解析為 D3DXLoadPRTBufferFromFileA。</span><span class="sxs-lookup"><span data-stu-id="8a0f5-120">Otherwise, the function call resolves to D3DXLoadPRTBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0f5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a0f5-121">Requirements</span></span>



| <span data-ttu-id="8a0f5-122">需求</span><span class="sxs-lookup"><span data-stu-id="8a0f5-122">Requirement</span></span> | <span data-ttu-id="8a0f5-123">值</span><span class="sxs-lookup"><span data-stu-id="8a0f5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0f5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8a0f5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8a0f5-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0f5-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8a0f5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8a0f5-126">Library</span></span><br/> | <dl> <span data-ttu-id="8a0f5-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a0f5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a0f5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a0f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0f5-129">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="8a0f5-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
