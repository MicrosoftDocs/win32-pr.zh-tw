---
description: 設定追蹤描述。
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: 'ID3DXAnimationController：： SetTrackDesc 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1aca9385f1e9bc9439b9fe4b3dc1acddda94e395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976514"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a><span data-ttu-id="956ec-103">ID3DXAnimationController：： SetTrackDesc 方法</span><span class="sxs-lookup"><span data-stu-id="956ec-103">ID3DXAnimationController::SetTrackDesc method</span></span>

<span data-ttu-id="956ec-104">設定追蹤描述。</span><span class="sxs-lookup"><span data-stu-id="956ec-104">Sets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="956ec-105">語法</span><span class="sxs-lookup"><span data-stu-id="956ec-105">Syntax</span></span>


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="956ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="956ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956ec-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="956ec-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="956ec-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="956ec-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="956ec-109">要修改之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="956ec-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="956ec-110">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="956ec-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="956ec-111">類型： **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="956ec-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="956ec-112">追蹤的描述。</span><span class="sxs-lookup"><span data-stu-id="956ec-112">Description of the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956ec-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="956ec-113">Return value</span></span>

<span data-ttu-id="956ec-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="956ec-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="956ec-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="956ec-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="956ec-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="956ec-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="956ec-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="956ec-117">Requirements</span></span>



| <span data-ttu-id="956ec-118">需求</span><span class="sxs-lookup"><span data-stu-id="956ec-118">Requirement</span></span> | <span data-ttu-id="956ec-119">值</span><span class="sxs-lookup"><span data-stu-id="956ec-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="956ec-120">標頭</span><span class="sxs-lookup"><span data-stu-id="956ec-120">Header</span></span><br/>  | <dl> <span data-ttu-id="956ec-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="956ec-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="956ec-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="956ec-122">Library</span></span><br/> | <dl> <span data-ttu-id="956ec-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="956ec-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="956ec-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="956ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956ec-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="956ec-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
