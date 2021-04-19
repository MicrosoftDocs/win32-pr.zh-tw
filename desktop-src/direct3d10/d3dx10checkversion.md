---
description: 確認您用來編譯的 D3DX 版本是您正在執行的版本。
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: 'D3DX10CheckVersion 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974886"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="1cd06-103">D3DX10CheckVersion 函式</span><span class="sxs-lookup"><span data-stu-id="1cd06-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="1cd06-104">確認您用來編譯的 D3DX 版本是您正在執行的版本。</span><span class="sxs-lookup"><span data-stu-id="1cd06-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd06-105">語法</span><span class="sxs-lookup"><span data-stu-id="1cd06-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="1cd06-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cd06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd06-107">*D3DSdkVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cd06-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd06-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cd06-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cd06-109">使用 D3D10 \_ SDK \_ 版本。</span><span class="sxs-lookup"><span data-stu-id="1cd06-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="1cd06-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1cd06-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cd06-111">*D3DX10SdkVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cd06-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd06-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cd06-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cd06-113">使用 D3DX10 \_ SDK \_ 版本。</span><span class="sxs-lookup"><span data-stu-id="1cd06-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="1cd06-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1cd06-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd06-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cd06-115">Return value</span></span>

<span data-ttu-id="1cd06-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cd06-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cd06-117">如果版本不相符，則函式會傳回 FALSE (小於或等於0的數位，數位本身沒有任何意義) 。</span><span class="sxs-lookup"><span data-stu-id="1cd06-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd06-118">備註</span><span class="sxs-lookup"><span data-stu-id="1cd06-118">Remarks</span></span>

<span data-ttu-id="1cd06-119">在您的應用程式初始化期間，請使用此函數。</span><span class="sxs-lookup"><span data-stu-id="1cd06-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="1cd06-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cd06-120">Requirements</span></span>



| <span data-ttu-id="1cd06-121">需求</span><span class="sxs-lookup"><span data-stu-id="1cd06-121">Requirement</span></span> | <span data-ttu-id="1cd06-122">值</span><span class="sxs-lookup"><span data-stu-id="1cd06-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd06-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1cd06-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1cd06-124"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd06-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="1cd06-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cd06-125">Library</span></span><br/> | <dl> <span data-ttu-id="1cd06-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cd06-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cd06-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cd06-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd06-128">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="1cd06-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
