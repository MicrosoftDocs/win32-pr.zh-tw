---
description: 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'ID3DXEffect：： OnLostDevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af2d17c99f0b694a8b27924c34faa2a1f633fafb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988172"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="61b2e-104">ID3DXEffect：： OnLostDevice 方法</span><span class="sxs-lookup"><span data-stu-id="61b2e-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="61b2e-105">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="61b2e-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="61b2e-106">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="61b2e-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="61b2e-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="61b2e-108">參數</span><span class="sxs-lookup"><span data-stu-id="61b2e-108">Parameters</span></span>

<span data-ttu-id="61b2e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="61b2e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61b2e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="61b2e-110">Return value</span></span>

<span data-ttu-id="61b2e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61b2e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61b2e-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="61b2e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="61b2e-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="61b2e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b2e-114">備註</span><span class="sxs-lookup"><span data-stu-id="61b2e-114">Remarks</span></span>

<span data-ttu-id="61b2e-115">只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)，就應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="61b2e-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="61b2e-116">即使裝置真的沒有遺失， **ID3DXEffect：： OnLostDevice** 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。</span><span class="sxs-lookup"><span data-stu-id="61b2e-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="61b2e-117">因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 [**ID3DXEffect：： OnResetDevice**](id3dxeffect--onresetdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="61b2e-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61b2e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="61b2e-118">Requirements</span></span>



| <span data-ttu-id="61b2e-119">需求</span><span class="sxs-lookup"><span data-stu-id="61b2e-119">Requirement</span></span> | <span data-ttu-id="61b2e-120">值</span><span class="sxs-lookup"><span data-stu-id="61b2e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b2e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="61b2e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="61b2e-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="61b2e-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="61b2e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="61b2e-123">Library</span></span><br/> | <dl> <span data-ttu-id="61b2e-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61b2e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="61b2e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61b2e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b2e-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="61b2e-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




