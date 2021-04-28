---
description: ID3DXRenderToSurface：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: 'ID3DXRenderToSurface：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093109"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a><span data-ttu-id="70971-104">ID3DXRenderToSurface：： OnLostDevice 方法</span><span class="sxs-lookup"><span data-stu-id="70971-104">ID3DXRenderToSurface::OnLostDevice method</span></span>

<span data-ttu-id="70971-105">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="70971-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="70971-106">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70971-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="70971-107">語法</span><span class="sxs-lookup"><span data-stu-id="70971-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="70971-108">參數</span><span class="sxs-lookup"><span data-stu-id="70971-108">Parameters</span></span>

<span data-ttu-id="70971-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="70971-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70971-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="70971-110">Return value</span></span>

<span data-ttu-id="70971-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70971-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70971-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="70971-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="70971-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="70971-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="70971-114">備註</span><span class="sxs-lookup"><span data-stu-id="70971-114">Remarks</span></span>

<span data-ttu-id="70971-115">只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)，就應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70971-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span></span> <span data-ttu-id="70971-116">即使裝置真的沒有遺失，ID3DXRenderToSurface：： OnLostDevice 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。</span><span class="sxs-lookup"><span data-stu-id="70971-116">Even if the device was not actually lost, ID3DXRenderToSurface::OnLostDevice is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="70971-117">因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 ID3DXRenderToSurface：： OnResetDevice。</span><span class="sxs-lookup"><span data-stu-id="70971-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then ID3DXRenderToSurface::OnResetDevice.</span></span>

## <a name="requirements"></a><span data-ttu-id="70971-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="70971-118">Requirements</span></span>



| <span data-ttu-id="70971-119">需求</span><span class="sxs-lookup"><span data-stu-id="70971-119">Requirement</span></span> | <span data-ttu-id="70971-120">值</span><span class="sxs-lookup"><span data-stu-id="70971-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70971-121">標頭</span><span class="sxs-lookup"><span data-stu-id="70971-121">Header</span></span><br/>  | <dl> <span data-ttu-id="70971-122"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="70971-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="70971-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="70971-123">Library</span></span><br/> | <dl> <span data-ttu-id="70971-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="70971-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70971-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70971-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70971-126">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="70971-126">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
