---
description: 將壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: 'D3DXSavePRTCompBufferToFile 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946088"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="05c8e-103">D3DXSavePRTCompBufferToFile 函式</span><span class="sxs-lookup"><span data-stu-id="05c8e-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="05c8e-104">將壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="05c8e-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c8e-105">語法</span><span class="sxs-lookup"><span data-stu-id="05c8e-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="05c8e-106">參數</span><span class="sxs-lookup"><span data-stu-id="05c8e-106">Parameters</span></span>

<span data-ttu-id="05c8e-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05c8e-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="05c8e-108">類型： **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05c8e-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05c8e-109">要儲存壓縮緩衝區的檔案名。</span><span class="sxs-lookup"><span data-stu-id="05c8e-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="05c8e-110">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05c8e-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="05c8e-111">類型： **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="05c8e-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="05c8e-112">輸入 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="05c8e-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="05c8e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="05c8e-113">Return value</span></span>

<span data-ttu-id="05c8e-114">類型： **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="05c8e-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="05c8e-115">如果方法成功，則傳回值為「 **D3D \_ 正常**」。</span><span class="sxs-lookup"><span data-stu-id="05c8e-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="05c8e-116">如果方法失敗，則傳回值可以是 **D3DERR \_ INVALIDCALL**。</span><span class="sxs-lookup"><span data-stu-id="05c8e-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c8e-117">備註</span><span class="sxs-lookup"><span data-stu-id="05c8e-117">Remarks</span></span>

<span data-ttu-id="05c8e-118">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="05c8e-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="05c8e-119">如果已定義 Unicode，則函式呼叫會解析為 [D3DXSavePRTCompBufferToFileW]()。</span><span class="sxs-lookup"><span data-stu-id="05c8e-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="05c8e-120">否則，函式呼叫會解析為 **D3DXSavePRTCompBufferToFileA**。</span><span class="sxs-lookup"><span data-stu-id="05c8e-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="05c8e-121">PCA 檔案格式是一種二進位檔案，格式為標頭，再接著兩個或三個數據區塊。</span><span class="sxs-lookup"><span data-stu-id="05c8e-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="05c8e-122">如果 *bIsTex* 不是零， *NumSamples* 應該相等 `TexWidth * TexHeight` 。</span><span class="sxs-lookup"><span data-stu-id="05c8e-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="05c8e-123">標頭之後的基礎資料區塊是 `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` 位元組。</span><span class="sxs-lookup"><span data-stu-id="05c8e-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="05c8e-124">以下是 PCA 加權資料區塊，也就是 `NumPCA * NumSamples * sizeof(float)` 位元組。</span><span class="sxs-lookup"><span data-stu-id="05c8e-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="05c8e-125">如果 *NumClusters* 大於1，檔案就會以位元組的叢集識別碼資料區塊結尾 `NumSamples * sizeof(UINT)` 。</span><span class="sxs-lookup"><span data-stu-id="05c8e-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c8e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="05c8e-126">Requirements</span></span>

| <span data-ttu-id="05c8e-127">需求</span><span class="sxs-lookup"><span data-stu-id="05c8e-127">Requirement</span></span> | <span data-ttu-id="05c8e-128">值</span><span class="sxs-lookup"><span data-stu-id="05c8e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05c8e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="05c8e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="05c8e-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="05c8e-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="05c8e-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="05c8e-131">Library</span></span><br/> | <dl> <span data-ttu-id="05c8e-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05c8e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="05c8e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05c8e-133">See also</span></span>

[<span data-ttu-id="05c8e-134">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="05c8e-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
