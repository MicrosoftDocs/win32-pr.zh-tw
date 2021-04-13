---
description: 設定可啟用或停用動畫播放軌的事件索引鍵。
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController：： KeyTrackEnable 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322679"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="07c91-103">ID3DXAnimationController：： KeyTrackEnable 方法</span><span class="sxs-lookup"><span data-stu-id="07c91-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="07c91-104">設定可啟用或停用動畫播放軌的事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="07c91-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c91-105">語法</span><span class="sxs-lookup"><span data-stu-id="07c91-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="07c91-106">參數</span><span class="sxs-lookup"><span data-stu-id="07c91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c91-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07c91-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c91-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c91-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07c91-109">要修改之動畫播放軌的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07c91-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="07c91-110">*NewEnable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07c91-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c91-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c91-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07c91-112">啟用旗標。</span><span class="sxs-lookup"><span data-stu-id="07c91-112">Enable flag.</span></span> <span data-ttu-id="07c91-113">將此設為 **TRUE** 以啟用動畫播放軌，或設定為 **FALSE** 以停用曲目。</span><span class="sxs-lookup"><span data-stu-id="07c91-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="07c91-114">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07c91-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c91-115">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07c91-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07c91-116">全域時間索引鍵。</span><span class="sxs-lookup"><span data-stu-id="07c91-116">Global time key.</span></span> <span data-ttu-id="07c91-117">指定將進行變更的全域時間。</span><span class="sxs-lookup"><span data-stu-id="07c91-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c91-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="07c91-118">Return value</span></span>

<span data-ttu-id="07c91-119">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="07c91-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="07c91-120">優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="07c91-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="07c91-121">如果 Track 無效，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="07c91-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c91-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="07c91-122">Requirements</span></span>



| <span data-ttu-id="07c91-123">需求</span><span class="sxs-lookup"><span data-stu-id="07c91-123">Requirement</span></span> | <span data-ttu-id="07c91-124">值</span><span class="sxs-lookup"><span data-stu-id="07c91-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07c91-125">標頭</span><span class="sxs-lookup"><span data-stu-id="07c91-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07c91-126"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="07c91-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="07c91-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="07c91-127">Library</span></span><br/> | <dl> <span data-ttu-id="07c91-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07c91-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07c91-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07c91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c91-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="07c91-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
