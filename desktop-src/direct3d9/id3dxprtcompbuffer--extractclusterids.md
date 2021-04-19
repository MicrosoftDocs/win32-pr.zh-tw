---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer：： ExtractClusterIDs 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989230"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="1a622-103">ID3DXPRTCompBuffer：： ExtractClusterIDs 方法</span><span class="sxs-lookup"><span data-stu-id="1a622-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="1a622-104">從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a622-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a622-105">語法</span><span class="sxs-lookup"><span data-stu-id="1a622-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="1a622-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a622-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a622-107">*pClusterIDs* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1a622-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a622-108">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a622-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1a622-109">寫入識別碼之記憶體位置的指標。</span><span class="sxs-lookup"><span data-stu-id="1a622-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="1a622-110">所需的記憶體長度是 [**ID3DXPRTCompBuffer：： GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="1a622-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a622-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a622-111">Return value</span></span>

<span data-ttu-id="1a622-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a622-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a622-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1a622-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1a622-114">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="1a622-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a622-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a622-115">Requirements</span></span>



| <span data-ttu-id="1a622-116">需求</span><span class="sxs-lookup"><span data-stu-id="1a622-116">Requirement</span></span> | <span data-ttu-id="1a622-117">值</span><span class="sxs-lookup"><span data-stu-id="1a622-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a622-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1a622-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1a622-119"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a622-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1a622-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a622-120">Library</span></span><br/> | <dl> <span data-ttu-id="1a622-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a622-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a622-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a622-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a622-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="1a622-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
