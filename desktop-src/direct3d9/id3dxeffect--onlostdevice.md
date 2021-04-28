---
description: ID3DXEffect：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
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
ms.openlocfilehash: 1aacdbae268b58a966256a99081b9943d0bfcc92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114966"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="4b8fc-104">ID3DXEffect：： OnLostDevice 方法</span><span class="sxs-lookup"><span data-stu-id="4b8fc-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="4b8fc-105">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="4b8fc-106">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="4b8fc-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="4b8fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b8fc-108">Parameters</span></span>

<span data-ttu-id="4b8fc-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b8fc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b8fc-110">Return value</span></span>

<span data-ttu-id="4b8fc-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b8fc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b8fc-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4b8fc-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8fc-114">備註</span><span class="sxs-lookup"><span data-stu-id="4b8fc-114">Remarks</span></span>

<span data-ttu-id="4b8fc-115">只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)，就應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="4b8fc-116">即使裝置真的沒有遺失， **ID3DXEffect：： OnLostDevice** 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="4b8fc-117">因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 [**ID3DXEffect：： OnResetDevice**](id3dxeffect--onresetdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8fc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b8fc-118">Requirements</span></span>



| <span data-ttu-id="4b8fc-119">需求</span><span class="sxs-lookup"><span data-stu-id="4b8fc-119">Requirement</span></span> | <span data-ttu-id="4b8fc-120">值</span><span class="sxs-lookup"><span data-stu-id="4b8fc-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8fc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4b8fc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4b8fc-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8fc-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4b8fc-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b8fc-123">Library</span></span><br/> | <dl> <span data-ttu-id="4b8fc-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b8fc-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4b8fc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b8fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8fc-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="4b8fc-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




