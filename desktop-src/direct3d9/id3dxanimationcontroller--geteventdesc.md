---
description: 取得指定動畫事件的描述。
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController：： GetEventDesc 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974892"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="66474-103">ID3DXAnimationController：： GetEventDesc 方法</span><span class="sxs-lookup"><span data-stu-id="66474-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="66474-104">取得指定動畫事件的描述。</span><span class="sxs-lookup"><span data-stu-id="66474-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="66474-105">語法</span><span class="sxs-lookup"><span data-stu-id="66474-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="66474-106">參數</span><span class="sxs-lookup"><span data-stu-id="66474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66474-107">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66474-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66474-108">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="66474-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="66474-109">要描述的動畫事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="66474-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="66474-110">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66474-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66474-111">類型： **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="66474-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="66474-112">[**D3DXEVENT \_ DESC**](d3dxevent-desc.md)結構的指標，其中包含動畫事件的描述。</span><span class="sxs-lookup"><span data-stu-id="66474-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66474-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="66474-113">Return value</span></span>

<span data-ttu-id="66474-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66474-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66474-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="66474-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="66474-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="66474-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="66474-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="66474-117">Requirements</span></span>



| <span data-ttu-id="66474-118">需求</span><span class="sxs-lookup"><span data-stu-id="66474-118">Requirement</span></span> | <span data-ttu-id="66474-119">值</span><span class="sxs-lookup"><span data-stu-id="66474-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66474-120">標頭</span><span class="sxs-lookup"><span data-stu-id="66474-120">Header</span></span><br/>  | <dl> <span data-ttu-id="66474-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="66474-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="66474-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="66474-122">Library</span></span><br/> | <dl> <span data-ttu-id="66474-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66474-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66474-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66474-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66474-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="66474-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




