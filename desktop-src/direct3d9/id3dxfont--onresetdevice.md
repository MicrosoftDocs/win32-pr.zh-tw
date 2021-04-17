---
description: 您可以使用這個方法來重新取得資源，並儲存初始狀態。
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'ID3DXFont：： OnResetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6e65001f484ed7d7a984ed1f9463b996056e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386481"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="2a92d-103">ID3DXFont：： OnResetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="2a92d-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="2a92d-104">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="2a92d-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a92d-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a92d-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="2a92d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a92d-106">Parameters</span></span>

<span data-ttu-id="2a92d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2a92d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a92d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a92d-108">Return value</span></span>

<span data-ttu-id="2a92d-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a92d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a92d-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2a92d-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a92d-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2a92d-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a92d-112">備註</span><span class="sxs-lookup"><span data-stu-id="2a92d-112">Remarks</span></span>

<span data-ttu-id="2a92d-113">在呼叫任何其他方法之前，每次使用 [**重設**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset))  (重設裝置時，都應該呼叫 **OnResetDevice** 。</span><span class="sxs-lookup"><span data-stu-id="2a92d-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="2a92d-114">這是重新取得影片記憶體資源和捕捉狀態欄塊的絕佳位置。</span><span class="sxs-lookup"><span data-stu-id="2a92d-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a92d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a92d-115">Requirements</span></span>



| <span data-ttu-id="2a92d-116">需求</span><span class="sxs-lookup"><span data-stu-id="2a92d-116">Requirement</span></span> | <span data-ttu-id="2a92d-117">值</span><span class="sxs-lookup"><span data-stu-id="2a92d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a92d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2a92d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2a92d-119"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a92d-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2a92d-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a92d-120">Library</span></span><br/> | <dl> <span data-ttu-id="2a92d-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a92d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a92d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a92d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a92d-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="2a92d-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
