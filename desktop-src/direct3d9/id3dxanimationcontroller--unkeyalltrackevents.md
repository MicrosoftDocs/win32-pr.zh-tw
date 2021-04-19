---
description: 從指定的動畫播放軌移除所有事件。
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'ID3DXAnimationController：： UnkeyAllTrackEvents 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986130"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="bddf3-103">ID3DXAnimationController：： UnkeyAllTrackEvents 方法</span><span class="sxs-lookup"><span data-stu-id="bddf3-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="bddf3-104">從指定的動畫播放軌移除所有事件。</span><span class="sxs-lookup"><span data-stu-id="bddf3-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddf3-105">語法</span><span class="sxs-lookup"><span data-stu-id="bddf3-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="bddf3-106">參數</span><span class="sxs-lookup"><span data-stu-id="bddf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bddf3-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bddf3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bddf3-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bddf3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bddf3-109">應移除所有事件之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bddf3-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bddf3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bddf3-110">Return value</span></span>

<span data-ttu-id="bddf3-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bddf3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bddf3-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bddf3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bddf3-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bddf3-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bddf3-114">備註</span><span class="sxs-lookup"><span data-stu-id="bddf3-114">Remarks</span></span>

<span data-ttu-id="bddf3-115">這個方法會防止執行之前排定在追蹤上的所有事件，並捨棄所有與這些事件相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="bddf3-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddf3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddf3-116">Requirements</span></span>



| <span data-ttu-id="bddf3-117">需求</span><span class="sxs-lookup"><span data-stu-id="bddf3-117">Requirement</span></span> | <span data-ttu-id="bddf3-118">值</span><span class="sxs-lookup"><span data-stu-id="bddf3-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bddf3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bddf3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bddf3-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="bddf3-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bddf3-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bddf3-121">Library</span></span><br/> | <dl> <span data-ttu-id="bddf3-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bddf3-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bddf3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddf3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddf3-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="bddf3-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
