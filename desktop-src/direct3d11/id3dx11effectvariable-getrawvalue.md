---
title: 'ID3DX11EffectVariable GetRawValue 方法 (D3dx11effect .h) '
description: 取得資料。
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- GetRawValue 方法 Direct3D 11
- GetRawValue 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetRawValue 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974689"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a><span data-ttu-id="00dbf-106">ID3DX11EffectVariable：： GetRawValue 方法</span><span class="sxs-lookup"><span data-stu-id="00dbf-106">ID3DX11EffectVariable::GetRawValue method</span></span>

<span data-ttu-id="00dbf-107">取得資料。</span><span class="sxs-lookup"><span data-stu-id="00dbf-107">Get data.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dbf-108">語法</span><span class="sxs-lookup"><span data-stu-id="00dbf-108">Syntax</span></span>


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="00dbf-109">參數</span><span class="sxs-lookup"><span data-stu-id="00dbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00dbf-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="00dbf-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="00dbf-111">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="00dbf-111">Type: **void\***</span></span>

<span data-ttu-id="00dbf-112">變數的指標。</span><span class="sxs-lookup"><span data-stu-id="00dbf-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="00dbf-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="00dbf-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="00dbf-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00dbf-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00dbf-115">從資料指標的開頭算起的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="00dbf-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="00dbf-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="00dbf-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="00dbf-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00dbf-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00dbf-118">要取得的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="00dbf-118">The number of bytes to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00dbf-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="00dbf-119">Return value</span></span>

<span data-ttu-id="00dbf-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00dbf-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00dbf-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="00dbf-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00dbf-122">備註</span><span class="sxs-lookup"><span data-stu-id="00dbf-122">Remarks</span></span>

<span data-ttu-id="00dbf-123">這個方法不會進行轉換或類型檢查;因此，它是存取陣列專案的快速方式。</span><span class="sxs-lookup"><span data-stu-id="00dbf-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="00dbf-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="00dbf-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="00dbf-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="00dbf-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="00dbf-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="00dbf-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00dbf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="00dbf-127">Requirements</span></span>



| <span data-ttu-id="00dbf-128">需求</span><span class="sxs-lookup"><span data-stu-id="00dbf-128">Requirement</span></span> | <span data-ttu-id="00dbf-129">值</span><span class="sxs-lookup"><span data-stu-id="00dbf-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00dbf-130">標頭</span><span class="sxs-lookup"><span data-stu-id="00dbf-130">Header</span></span><br/>  | <dl> <span data-ttu-id="00dbf-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="00dbf-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="00dbf-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="00dbf-132">Library</span></span><br/> | <dl> <span data-ttu-id="00dbf-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="00dbf-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00dbf-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00dbf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dbf-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="00dbf-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

