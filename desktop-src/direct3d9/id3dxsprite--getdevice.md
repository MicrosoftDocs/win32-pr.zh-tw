---
description: 捕獲與 sprite 物件相關聯的裝置。
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'ID3DXSprite：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386491"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="9267a-103">ID3DXSprite：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="9267a-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="9267a-104">捕獲與 sprite 物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="9267a-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9267a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9267a-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9267a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9267a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9267a-107">*ppDevice* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="9267a-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9267a-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="9267a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="9267a-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與 sprite 物件相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="9267a-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9267a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9267a-110">Return value</span></span>

<span data-ttu-id="9267a-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9267a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9267a-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9267a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9267a-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9267a-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="9267a-114">備註</span><span class="sxs-lookup"><span data-stu-id="9267a-114">Remarks</span></span>

<span data-ttu-id="9267a-115">呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="9267a-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9267a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9267a-116">Requirements</span></span>



| <span data-ttu-id="9267a-117">需求</span><span class="sxs-lookup"><span data-stu-id="9267a-117">Requirement</span></span> | <span data-ttu-id="9267a-118">值</span><span class="sxs-lookup"><span data-stu-id="9267a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9267a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9267a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9267a-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="9267a-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9267a-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="9267a-121">Library</span></span><br/> | <dl> <span data-ttu-id="9267a-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9267a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9267a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9267a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9267a-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="9267a-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
