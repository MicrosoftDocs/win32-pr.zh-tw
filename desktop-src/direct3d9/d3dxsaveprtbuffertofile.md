---
description: 將預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: 'D3DXSavePRTBufferToFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985883"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="2079e-103">D3DXSavePRTBufferToFile 函式</span><span class="sxs-lookup"><span data-stu-id="2079e-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="2079e-104">將預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="2079e-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="2079e-105">語法</span><span class="sxs-lookup"><span data-stu-id="2079e-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="2079e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2079e-106">Parameters</span></span>

<span data-ttu-id="2079e-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2079e-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="2079e-108">類型： **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2079e-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2079e-109">要儲存緩衝區的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2079e-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="2079e-110">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2079e-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="2079e-111">類型： **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2079e-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2079e-112">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="2079e-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="2079e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2079e-113">Return value</span></span>

<span data-ttu-id="2079e-114">類型： **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2079e-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2079e-115">如果方法成功，則傳回值為「 **D3D \_ 正常**」。</span><span class="sxs-lookup"><span data-stu-id="2079e-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="2079e-116">如果方法失敗，則傳回值可以是 **D3DERR \_ INVALIDCALL**。</span><span class="sxs-lookup"><span data-stu-id="2079e-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2079e-117">備註</span><span class="sxs-lookup"><span data-stu-id="2079e-117">Remarks</span></span>

<span data-ttu-id="2079e-118">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="2079e-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2079e-119">如果已定義 Unicode，則函式呼叫會解析為 [D3DXSavePRTBufferToFileW]()。</span><span class="sxs-lookup"><span data-stu-id="2079e-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="2079e-120">否則，函式呼叫會解析為 **D3DXSavePRTBufferToFileA**。</span><span class="sxs-lookup"><span data-stu-id="2079e-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="2079e-121">PRT 檔案格式是一種二進位檔案，其格式為標頭，然後是資料區塊。</span><span class="sxs-lookup"><span data-stu-id="2079e-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="2079e-122">如果 *bIsTex* 不是零， *NumSamples* 應該相等 `TexWidth * TexHeight` 。</span><span class="sxs-lookup"><span data-stu-id="2079e-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="2079e-123">標頭之後的資料區塊是 `NumSamples * NumCoeffs * NumChannels * sizeof(float)` 位元組。</span><span class="sxs-lookup"><span data-stu-id="2079e-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2079e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2079e-124">Requirements</span></span>

| <span data-ttu-id="2079e-125">需求</span><span class="sxs-lookup"><span data-stu-id="2079e-125">Requirement</span></span> | <span data-ttu-id="2079e-126">值</span><span class="sxs-lookup"><span data-stu-id="2079e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2079e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2079e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2079e-128"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2079e-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2079e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2079e-129">Library</span></span><br/> | <dl> <span data-ttu-id="2079e-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2079e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="2079e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2079e-131">See also</span></span>

[<span data-ttu-id="2079e-132">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="2079e-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
