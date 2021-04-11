---
description: 啟用或停用動畫控制器中的軌跡。
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController：： SetTrackEnable 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035404"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="ee1b7-103">ID3DXAnimationController：： SetTrackEnable 方法</span><span class="sxs-lookup"><span data-stu-id="ee1b7-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="ee1b7-104">啟用或停用動畫控制器中的軌跡。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee1b7-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="ee1b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee1b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1b7-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee1b7-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1b7-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee1b7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee1b7-109">要混合之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="ee1b7-110">*啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee1b7-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1b7-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee1b7-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee1b7-112">啟用值。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-112">Enable value.</span></span> <span data-ttu-id="ee1b7-113">設定為 **TRUE** 可在控制器中啟用此追蹤，或設為 **FALSE** 以防止其混合。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1b7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee1b7-114">Return value</span></span>

<span data-ttu-id="ee1b7-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee1b7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee1b7-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ee1b7-117">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1b7-118">備註</span><span class="sxs-lookup"><span data-stu-id="ee1b7-118">Remarks</span></span>

<span data-ttu-id="ee1b7-119">若要混用追蹤與其他曲目，啟用旗標必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="ee1b7-120">相反地，將旗標設定為 **FALSE** 將會防止追蹤與其他曲目混合。</span><span class="sxs-lookup"><span data-stu-id="ee1b7-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1b7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee1b7-121">Requirements</span></span>



| <span data-ttu-id="ee1b7-122">需求</span><span class="sxs-lookup"><span data-stu-id="ee1b7-122">Requirement</span></span> | <span data-ttu-id="ee1b7-123">值</span><span class="sxs-lookup"><span data-stu-id="ee1b7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1b7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ee1b7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ee1b7-125"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee1b7-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ee1b7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee1b7-126">Library</span></span><br/> | <dl> <span data-ttu-id="ee1b7-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee1b7-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee1b7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee1b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1b7-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ee1b7-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
