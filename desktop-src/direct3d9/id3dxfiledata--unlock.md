---
description: 結束 ID3DXFileData：： Lock 所傳回之 ppData 指標的存留期。
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData：： Unlock 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696704"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="ec75b-103">ID3DXFileData：： Unlock 方法</span><span class="sxs-lookup"><span data-stu-id="ec75b-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="ec75b-104">結束 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md)所傳回之 *ppData* 指標的存留期。</span><span class="sxs-lookup"><span data-stu-id="ec75b-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec75b-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec75b-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="ec75b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec75b-106">Parameters</span></span>

<span data-ttu-id="ec75b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ec75b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec75b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec75b-108">Return value</span></span>

<span data-ttu-id="ec75b-109">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec75b-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec75b-110">傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ec75b-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec75b-111">備註</span><span class="sxs-lookup"><span data-stu-id="ec75b-111">Remarks</span></span>

<span data-ttu-id="ec75b-112">您必須確保 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md) 呼叫的數目符合 **ID3DXFileData：： Unlock** 呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="ec75b-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="ec75b-113">呼叫 Unlock 之後，不應該再使用 **ID3DXFileData：： Lock** 所傳回的 ppData 指標。</span><span class="sxs-lookup"><span data-stu-id="ec75b-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec75b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec75b-114">Requirements</span></span>



| <span data-ttu-id="ec75b-115">需求</span><span class="sxs-lookup"><span data-stu-id="ec75b-115">Requirement</span></span> | <span data-ttu-id="ec75b-116">值</span><span class="sxs-lookup"><span data-stu-id="ec75b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec75b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ec75b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ec75b-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec75b-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ec75b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec75b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ec75b-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec75b-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ec75b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec75b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec75b-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="ec75b-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
