---
description: 使用記憶體複製來設定著色器常數的連續範圍。
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect：： SetRawValue 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982198"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="bbf25-103">ID3DXEffect：： SetRawValue 方法</span><span class="sxs-lookup"><span data-stu-id="bbf25-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="bbf25-104">使用記憶體複製來設定著色器常數的連續範圍。</span><span class="sxs-lookup"><span data-stu-id="bbf25-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf25-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbf25-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="bbf25-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbf25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf25-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbf25-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf25-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bbf25-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bbf25-109">要設定之值的控制碼，或傳入做為字串的值名稱。</span><span class="sxs-lookup"><span data-stu-id="bbf25-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="bbf25-110">傳遞控制碼更有效率。</span><span class="sxs-lookup"><span data-stu-id="bbf25-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="bbf25-111">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf25-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf25-112">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbf25-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf25-113">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="bbf25-113">Type: **void\***</span></span>

<span data-ttu-id="bbf25-114">包含要設定之資料的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="bbf25-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="bbf25-115">SetRawValue 會檢查是否有有效的記憶體，但不會檢查是否有有效的資料。</span><span class="sxs-lookup"><span data-stu-id="bbf25-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="bbf25-116">*OffsetInBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbf25-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf25-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbf25-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbf25-118">效果資料開始與您要設定之效果常數開頭之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="bbf25-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="bbf25-119">*位元組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbf25-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf25-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbf25-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbf25-121">要設定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbf25-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf25-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbf25-122">Return value</span></span>

<span data-ttu-id="bbf25-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbf25-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbf25-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bbf25-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bbf25-125">如果方法失敗，則傳回值可以是下列其中一項： E \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bbf25-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf25-126">備註</span><span class="sxs-lookup"><span data-stu-id="bbf25-126">Remarks</span></span>

<span data-ttu-id="bbf25-127">SetRawValue 是設定效果常數的最快速方式，因為它會執行記憶體複製而不執行驗證或任何資料轉換 (例如將資料列主要矩陣轉換成資料行主要矩陣) 。</span><span class="sxs-lookup"><span data-stu-id="bbf25-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="bbf25-128">使用 SetRawValue 來設定一連串連續的效果常數。</span><span class="sxs-lookup"><span data-stu-id="bbf25-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="bbf25-129">例如，您可以設定20個矩陣的陣列，其中包含20個對 [**ID3DXBaseEffect：： SetMatrix**](id3dxbaseeffect--setmatrix.md) 的呼叫，或使用單一 SetRawValue。</span><span class="sxs-lookup"><span data-stu-id="bbf25-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="bbf25-130">所有值都必須是 matrix4x4s 或 float4s，而且所有矩陣都必須是資料行主要順序。</span><span class="sxs-lookup"><span data-stu-id="bbf25-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="bbf25-131">Int 或 float 值會轉換成 float4;因此，強烈建議您只搭配 float4 或 matrix4x4 資料使用 SetRawValue。</span><span class="sxs-lookup"><span data-stu-id="bbf25-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf25-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbf25-132">Requirements</span></span>



| <span data-ttu-id="bbf25-133">需求</span><span class="sxs-lookup"><span data-stu-id="bbf25-133">Requirement</span></span> | <span data-ttu-id="bbf25-134">值</span><span class="sxs-lookup"><span data-stu-id="bbf25-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf25-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bbf25-135">Header</span></span><br/>  | <dl> <span data-ttu-id="bbf25-136"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf25-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bbf25-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="bbf25-137">Library</span></span><br/> | <dl> <span data-ttu-id="bbf25-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbf25-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bbf25-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbf25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf25-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="bbf25-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
