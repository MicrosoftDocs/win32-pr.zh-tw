---
description: ID3DXLine：： OnLostDevice 方法-使用此方法釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: 'ID3DXLine：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f3845e40e4ece115704c38904a61dbca3c24443
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093676"
---
# <a name="id3dxlineonlostdevice-method"></a><span data-ttu-id="da93c-104">ID3DXLine：： OnLostDevice 方法</span><span class="sxs-lookup"><span data-stu-id="da93c-104">ID3DXLine::OnLostDevice method</span></span>

<span data-ttu-id="da93c-105">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="da93c-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="da93c-106">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="da93c-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="da93c-107">語法</span><span class="sxs-lookup"><span data-stu-id="da93c-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="da93c-108">參數</span><span class="sxs-lookup"><span data-stu-id="da93c-108">Parameters</span></span>

<span data-ttu-id="da93c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="da93c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da93c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="da93c-110">Return value</span></span>

<span data-ttu-id="da93c-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da93c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da93c-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="da93c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="da93c-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="da93c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="da93c-114">備註</span><span class="sxs-lookup"><span data-stu-id="da93c-114">Remarks</span></span>

<span data-ttu-id="da93c-115">只要裝置遺失或使用者呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)，就應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="da93c-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="da93c-116">即使裝置真的沒有遺失， **ID3DXLine：： OnLostDevice** 也負責釋放 stateblocks 和其他資源，在重設裝置之前可能需要先釋出這些資源。</span><span class="sxs-lookup"><span data-stu-id="da93c-116">Even if the device was not actually lost, **ID3DXLine::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="da93c-117">因此，在呼叫 **IDirect3DDevice9：： Reset** 之前無法再次使用字型物件，然後再呼叫 [**ID3DXLine：： OnResetDevice**](id3dxline--onresetdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="da93c-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da93c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="da93c-118">Requirements</span></span>



| <span data-ttu-id="da93c-119">需求</span><span class="sxs-lookup"><span data-stu-id="da93c-119">Requirement</span></span> | <span data-ttu-id="da93c-120">值</span><span class="sxs-lookup"><span data-stu-id="da93c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da93c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="da93c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="da93c-122"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="da93c-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="da93c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="da93c-123">Library</span></span><br/> | <dl> <span data-ttu-id="da93c-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da93c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da93c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da93c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da93c-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="da93c-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 




