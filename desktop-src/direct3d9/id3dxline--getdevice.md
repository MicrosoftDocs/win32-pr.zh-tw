---
description: 抓取與 line 物件相關聯的 Direct3D 裝置。
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'ID3DXLine：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999058"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="5ee42-103">ID3DXLine：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="5ee42-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="5ee42-104">抓取與 line 物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="5ee42-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee42-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ee42-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="5ee42-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ee42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee42-107">*ppDevice* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5ee42-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee42-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="5ee42-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="5ee42-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與 line 物件相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="5ee42-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ee42-110">Return value</span></span>

<span data-ttu-id="5ee42-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ee42-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ee42-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5ee42-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ee42-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="5ee42-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee42-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ee42-114">Requirements</span></span>



| <span data-ttu-id="5ee42-115">需求</span><span class="sxs-lookup"><span data-stu-id="5ee42-115">Requirement</span></span> | <span data-ttu-id="5ee42-116">值</span><span class="sxs-lookup"><span data-stu-id="5ee42-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee42-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5ee42-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5ee42-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee42-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5ee42-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="5ee42-119">Library</span></span><br/> | <dl> <span data-ttu-id="5ee42-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ee42-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ee42-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ee42-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee42-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="5ee42-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
