---
title: 'ID3DX11EffectVariable SetRawValue 方法 (D3dx11effect .h) '
description: 設定資料。
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- SetRawValue 方法 Direct3D 11
- SetRawValue 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，SetRawValue 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196188"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="270ac-106">ID3DX11EffectVariable：： SetRawValue 方法</span><span class="sxs-lookup"><span data-stu-id="270ac-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="270ac-107">設定資料。</span><span class="sxs-lookup"><span data-stu-id="270ac-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="270ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="270ac-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="270ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="270ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270ac-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="270ac-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="270ac-111">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="270ac-111">Type: **void\***</span></span>

<span data-ttu-id="270ac-112">變數的指標。</span><span class="sxs-lookup"><span data-stu-id="270ac-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="270ac-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="270ac-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="270ac-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="270ac-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="270ac-115">從資料指標的開頭算起的位移 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="270ac-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="270ac-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="270ac-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="270ac-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="270ac-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="270ac-118">要設定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="270ac-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270ac-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="270ac-119">Return value</span></span>

<span data-ttu-id="270ac-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="270ac-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="270ac-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="270ac-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="270ac-122">備註</span><span class="sxs-lookup"><span data-stu-id="270ac-122">Remarks</span></span>

<span data-ttu-id="270ac-123">這個方法不會進行轉換或類型檢查;因此，它是存取陣列專案的快速方式。</span><span class="sxs-lookup"><span data-stu-id="270ac-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="270ac-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="270ac-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="270ac-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="270ac-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="270ac-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="270ac-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="270ac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="270ac-127">Requirements</span></span>



| <span data-ttu-id="270ac-128">需求</span><span class="sxs-lookup"><span data-stu-id="270ac-128">Requirement</span></span> | <span data-ttu-id="270ac-129">值</span><span class="sxs-lookup"><span data-stu-id="270ac-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270ac-130">標頭</span><span class="sxs-lookup"><span data-stu-id="270ac-130">Header</span></span><br/>  | <dl> <span data-ttu-id="270ac-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="270ac-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="270ac-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="270ac-132">Library</span></span><br/> | <dl> <span data-ttu-id="270ac-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="270ac-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="270ac-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="270ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270ac-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="270ac-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

