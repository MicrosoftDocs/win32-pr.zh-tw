---
description: ID3DXEffect：： OnResetDevice 方法-使用此方法可重新取得資源並儲存初始狀態。
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'ID3DXEffect：： OnResetDevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a10d9d0a9092bf7a0fdd345cde8220675503acd0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114926"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="614dd-103">ID3DXEffect：： OnResetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="614dd-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="614dd-104">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="614dd-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="614dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="614dd-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="614dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="614dd-106">Parameters</span></span>

<span data-ttu-id="614dd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="614dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="614dd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="614dd-108">Return value</span></span>

<span data-ttu-id="614dd-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="614dd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="614dd-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="614dd-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="614dd-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="614dd-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="614dd-112">備註</span><span class="sxs-lookup"><span data-stu-id="614dd-112">Remarks</span></span>

<span data-ttu-id="614dd-113">在呼叫任何其他方法之前，請使用 [**IDirect3DDevice9：： reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) 來 (每次重設裝置時，都要呼叫 **ID3DXEffect：： OnResetDevice** 。</span><span class="sxs-lookup"><span data-stu-id="614dd-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="614dd-114">這是重新取得影片記憶體資源和捕捉狀態欄塊的絕佳位置。</span><span class="sxs-lookup"><span data-stu-id="614dd-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="614dd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="614dd-115">Requirements</span></span>



| <span data-ttu-id="614dd-116">需求</span><span class="sxs-lookup"><span data-stu-id="614dd-116">Requirement</span></span> | <span data-ttu-id="614dd-117">值</span><span class="sxs-lookup"><span data-stu-id="614dd-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="614dd-118">標頭</span><span class="sxs-lookup"><span data-stu-id="614dd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="614dd-119"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="614dd-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="614dd-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="614dd-120">Library</span></span><br/> | <dl> <span data-ttu-id="614dd-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="614dd-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="614dd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="614dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614dd-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="614dd-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
