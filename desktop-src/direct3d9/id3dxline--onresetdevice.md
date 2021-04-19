---
description: 您可以使用這個方法來重新取得資源，並儲存初始狀態。
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: 'ID3DXLine：： OnResetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c85a93084e3a4f3d8308e5111338d0c5127e22c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988226"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="75b3a-103">ID3DXLine：： OnResetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="75b3a-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="75b3a-104">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="75b3a-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="75b3a-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="75b3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="75b3a-106">Parameters</span></span>

<span data-ttu-id="75b3a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="75b3a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75b3a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="75b3a-108">Return value</span></span>

<span data-ttu-id="75b3a-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75b3a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75b3a-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="75b3a-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="75b3a-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="75b3a-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b3a-112">備註</span><span class="sxs-lookup"><span data-stu-id="75b3a-112">Remarks</span></span>

<span data-ttu-id="75b3a-113">在呼叫任何其他方法之前，請使用 [**IDirect3DDevice9：： reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) 來 (每次重設裝置時，都要呼叫 **ID3DXLine：： OnResetDevice** 。</span><span class="sxs-lookup"><span data-stu-id="75b3a-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="75b3a-114">這是重新取得影片記憶體資源和捕捉狀態欄塊的絕佳位置。</span><span class="sxs-lookup"><span data-stu-id="75b3a-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b3a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="75b3a-115">Requirements</span></span>



| <span data-ttu-id="75b3a-116">需求</span><span class="sxs-lookup"><span data-stu-id="75b3a-116">Requirement</span></span> | <span data-ttu-id="75b3a-117">值</span><span class="sxs-lookup"><span data-stu-id="75b3a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b3a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="75b3a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="75b3a-119"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="75b3a-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="75b3a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="75b3a-120">Library</span></span><br/> | <dl> <span data-ttu-id="75b3a-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75b3a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75b3a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75b3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b3a-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="75b3a-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
