---
description: 將常數設定為其預設值。 預設值會在著色器的變數宣告中宣告。
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'ID3DXConstantTable：： SetDefaults 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696659"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="bddfb-104">ID3DXConstantTable：： SetDefaults 方法</span><span class="sxs-lookup"><span data-stu-id="bddfb-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="bddfb-105">將常數設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="bddfb-105">Sets the constants to their default values.</span></span> <span data-ttu-id="bddfb-106">預設值會在著色器的變數宣告中宣告。</span><span class="sxs-lookup"><span data-stu-id="bddfb-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddfb-107">語法</span><span class="sxs-lookup"><span data-stu-id="bddfb-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bddfb-108">參數</span><span class="sxs-lookup"><span data-stu-id="bddfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bddfb-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bddfb-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bddfb-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bddfb-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bddfb-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="bddfb-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bddfb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bddfb-112">Return value</span></span>

<span data-ttu-id="bddfb-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bddfb-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bddfb-114">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bddfb-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bddfb-115">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bddfb-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddfb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddfb-116">Requirements</span></span>



| <span data-ttu-id="bddfb-117">需求</span><span class="sxs-lookup"><span data-stu-id="bddfb-117">Requirement</span></span> | <span data-ttu-id="bddfb-118">值</span><span class="sxs-lookup"><span data-stu-id="bddfb-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddfb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bddfb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bddfb-120"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="bddfb-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bddfb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bddfb-121">Library</span></span><br/> | <dl> <span data-ttu-id="bddfb-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bddfb-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bddfb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddfb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddfb-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="bddfb-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
