---
description: 取出與 sprite 物件相關聯的裝置。
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite：： GetDevice 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323423"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="17d83-103">ID3DX10Sprite：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="17d83-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="17d83-104">取出與 sprite 物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="17d83-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d83-105">語法</span><span class="sxs-lookup"><span data-stu-id="17d83-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="17d83-106">參數</span><span class="sxs-lookup"><span data-stu-id="17d83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d83-107">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17d83-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d83-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="17d83-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="17d83-109">ID3D10Device 介面指標的位址，表示與 sprite 物件相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="17d83-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d83-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="17d83-110">Return value</span></span>

<span data-ttu-id="17d83-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17d83-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17d83-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="17d83-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="17d83-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="17d83-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d83-114">備註</span><span class="sxs-lookup"><span data-stu-id="17d83-114">Remarks</span></span>

<span data-ttu-id="17d83-115">呼叫這個方法將會增加 ID3D10Device 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="17d83-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d83-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="17d83-116">Requirements</span></span>



| <span data-ttu-id="17d83-117">需求</span><span class="sxs-lookup"><span data-stu-id="17d83-117">Requirement</span></span> | <span data-ttu-id="17d83-118">值</span><span class="sxs-lookup"><span data-stu-id="17d83-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17d83-119">標頭</span><span class="sxs-lookup"><span data-stu-id="17d83-119">Header</span></span><br/>  | <dl> <span data-ttu-id="17d83-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="17d83-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="17d83-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="17d83-121">Library</span></span><br/> | <dl> <span data-ttu-id="17d83-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="17d83-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d83-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17d83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d83-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="17d83-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="17d83-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="17d83-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




