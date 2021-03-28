---
title: 'ID3DX11EffectStringVariable GetString 方法 (D3dx11effect .h) '
description: 取得字串。
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- GetString 方法 Direct3D 11
- GetString 方法 Direct3D 11，ID3DX11EffectStringVariable 介面
- ID3DX11EffectStringVariable 介面 Direct3D 11，GetString 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974472"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="0f9cd-106">ID3DX11EffectStringVariable：： GetString 方法</span><span class="sxs-lookup"><span data-stu-id="0f9cd-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="0f9cd-107">取得字串。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9cd-108">語法</span><span class="sxs-lookup"><span data-stu-id="0f9cd-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="0f9cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="0f9cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f9cd-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="0f9cd-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="0f9cd-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="0f9cd-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0f9cd-112">字串的指標。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f9cd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f9cd-113">Return value</span></span>

<span data-ttu-id="0f9cd-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f9cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f9cd-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f9cd-116">備註</span><span class="sxs-lookup"><span data-stu-id="0f9cd-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f9cd-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0f9cd-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0f9cd-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9cd-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f9cd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f9cd-120">Requirements</span></span>



| <span data-ttu-id="0f9cd-121">需求</span><span class="sxs-lookup"><span data-stu-id="0f9cd-121">Requirement</span></span> | <span data-ttu-id="0f9cd-122">值</span><span class="sxs-lookup"><span data-stu-id="0f9cd-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9cd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0f9cd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0f9cd-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f9cd-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0f9cd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f9cd-125">Library</span></span><br/> | <dl> <span data-ttu-id="0f9cd-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="0f9cd-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9cd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f9cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9cd-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="0f9cd-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

