---
description: 捕獲與環境對應相關聯的 Direct3D 裝置。
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: 'ID3DXRenderToEnvMap：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976474"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a><span data-ttu-id="3392e-103">ID3DXRenderToEnvMap：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="3392e-103">ID3DXRenderToEnvMap::GetDevice method</span></span>

<span data-ttu-id="3392e-104">捕獲與環境對應相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="3392e-104">Retrieves the Direct3D device associated with the environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="3392e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3392e-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="3392e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3392e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3392e-107">*ppDevice* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="3392e-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3392e-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="3392e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="3392e-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與環境對應相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="3392e-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface that represents the Direct3D device object associated with the environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3392e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3392e-110">Return value</span></span>

<span data-ttu-id="3392e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3392e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3392e-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3392e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3392e-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="3392e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="3392e-114">呼叫這個方法會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="3392e-114">Calling this method increases the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="3392e-115">當您使用這個 **IDirect3DDevice9** 介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="3392e-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="3392e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3392e-116">Requirements</span></span>



| <span data-ttu-id="3392e-117">需求</span><span class="sxs-lookup"><span data-stu-id="3392e-117">Requirement</span></span> | <span data-ttu-id="3392e-118">值</span><span class="sxs-lookup"><span data-stu-id="3392e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3392e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3392e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3392e-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="3392e-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3392e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3392e-121">Library</span></span><br/> | <dl> <span data-ttu-id="3392e-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3392e-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3392e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3392e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3392e-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="3392e-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
