---
description: 將軌跡設定為指定的本機動畫時間。
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController：： SetTrackPosition 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975701"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a><span data-ttu-id="67e6f-103">ID3DXAnimationController：： SetTrackPosition 方法</span><span class="sxs-lookup"><span data-stu-id="67e6f-103">ID3DXAnimationController::SetTrackPosition method</span></span>

<span data-ttu-id="67e6f-104">將軌跡設定為指定的本機動畫時間。</span><span class="sxs-lookup"><span data-stu-id="67e6f-104">Sets the track to the specified local animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e6f-105">語法</span><span class="sxs-lookup"><span data-stu-id="67e6f-105">Syntax</span></span>


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="67e6f-106">參數</span><span class="sxs-lookup"><span data-stu-id="67e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e6f-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67e6f-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67e6f-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67e6f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67e6f-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="67e6f-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="67e6f-110">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67e6f-110">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67e6f-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67e6f-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67e6f-112">要指派給追蹤的本機動畫時間值。</span><span class="sxs-lookup"><span data-stu-id="67e6f-112">Local animation time value to assign to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e6f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67e6f-113">Return value</span></span>

<span data-ttu-id="67e6f-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67e6f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67e6f-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="67e6f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="67e6f-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="67e6f-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="67e6f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="67e6f-117">Requirements</span></span>



| <span data-ttu-id="67e6f-118">需求</span><span class="sxs-lookup"><span data-stu-id="67e6f-118">Requirement</span></span> | <span data-ttu-id="67e6f-119">值</span><span class="sxs-lookup"><span data-stu-id="67e6f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67e6f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="67e6f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="67e6f-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="67e6f-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="67e6f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="67e6f-122">Library</span></span><br/> | <dl> <span data-ttu-id="67e6f-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="67e6f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67e6f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67e6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e6f-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="67e6f-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
