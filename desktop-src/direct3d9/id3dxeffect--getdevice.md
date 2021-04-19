---
description: 捕獲與效果相關聯的裝置。
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'ID3DXEffect：： GetDevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981861"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="d1c3c-103">ID3DXEffect：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="d1c3c-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="d1c3c-104">捕獲與效果相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c3c-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1c3c-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d1c3c-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1c3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c3c-107">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1c3c-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c3c-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="d1c3c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="d1c3c-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與效果相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c3c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1c3c-110">Return value</span></span>

<span data-ttu-id="d1c3c-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1c3c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1c3c-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d1c3c-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c3c-114">備註</span><span class="sxs-lookup"><span data-stu-id="d1c3c-114">Remarks</span></span>

<span data-ttu-id="d1c3c-115">呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="d1c3c-116">當您使用 **IDirect3DDevice9** 介面完成時，請務必呼叫 IUnknown：： Release，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="d1c3c-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c3c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1c3c-117">Requirements</span></span>



| <span data-ttu-id="d1c3c-118">需求</span><span class="sxs-lookup"><span data-stu-id="d1c3c-118">Requirement</span></span> | <span data-ttu-id="d1c3c-119">值</span><span class="sxs-lookup"><span data-stu-id="d1c3c-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c3c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d1c3c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d1c3c-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c3c-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d1c3c-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1c3c-122">Library</span></span><br/> | <dl> <span data-ttu-id="d1c3c-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1c3c-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d1c3c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1c3c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c3c-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="d1c3c-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
