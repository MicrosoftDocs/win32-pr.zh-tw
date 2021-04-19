---
description: 確認您用來編譯的 D3DX 版本是您正在執行的版本。
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: 'D3DXCheckVersion 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988196"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="31ab4-103">D3DXCheckVersion 函式</span><span class="sxs-lookup"><span data-stu-id="31ab4-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="31ab4-104">確認您用來編譯的 D3DX 版本是您正在執行的版本。</span><span class="sxs-lookup"><span data-stu-id="31ab4-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ab4-105">語法</span><span class="sxs-lookup"><span data-stu-id="31ab4-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="31ab4-106">參數</span><span class="sxs-lookup"><span data-stu-id="31ab4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ab4-107">*D3DSDKVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31ab4-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ab4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ab4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ab4-109">使用 D3D \_ SDK \_ 版本。</span><span class="sxs-lookup"><span data-stu-id="31ab4-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="31ab4-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="31ab4-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="31ab4-111">*D3DXSDKVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31ab4-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ab4-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ab4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ab4-113">使用 D3DX \_ SDK \_ 版本。</span><span class="sxs-lookup"><span data-stu-id="31ab4-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="31ab4-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="31ab4-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ab4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="31ab4-115">Return value</span></span>

<span data-ttu-id="31ab4-116">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ab4-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ab4-117">如果您編譯的 D3DX 版本是您正在執行的版本，則傳回 **TRUE** ;否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="31ab4-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ab4-118">備註</span><span class="sxs-lookup"><span data-stu-id="31ab4-118">Remarks</span></span>

<span data-ttu-id="31ab4-119">在應用程式初始化期間使用此函數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="31ab4-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="31ab4-120">使用 [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) 來確認是否已安裝正確的執行時間。</span><span class="sxs-lookup"><span data-stu-id="31ab4-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ab4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="31ab4-121">Requirements</span></span>



| <span data-ttu-id="31ab4-122">需求</span><span class="sxs-lookup"><span data-stu-id="31ab4-122">Requirement</span></span> | <span data-ttu-id="31ab4-123">值</span><span class="sxs-lookup"><span data-stu-id="31ab4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ab4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="31ab4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="31ab4-125"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="31ab4-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="31ab4-126">Library</span></span><br/> | <dl> <span data-ttu-id="31ab4-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31ab4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31ab4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ab4-129">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="31ab4-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
