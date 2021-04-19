---
description: 取出與字型物件相關聯的 Direct3D 裝置。
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font：： GetDevice 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986097"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="341fa-103">ID3DX10Font：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="341fa-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="341fa-104">取出與字型物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="341fa-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="341fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="341fa-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="341fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="341fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341fa-107">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="341fa-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="341fa-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="341fa-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="341fa-109">ID3D10Device 介面指標的位址，表示與字型物件相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="341fa-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341fa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="341fa-110">Return value</span></span>

<span data-ttu-id="341fa-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="341fa-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="341fa-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="341fa-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="341fa-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="341fa-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="341fa-114">備註</span><span class="sxs-lookup"><span data-stu-id="341fa-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="341fa-115">呼叫這個方法將會增加 ID3D10Device 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="341fa-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="341fa-116">當您使用這個 ID3D10Device 介面完成時，請務必呼叫 IUnknown，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="341fa-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="341fa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="341fa-117">Requirements</span></span>



| <span data-ttu-id="341fa-118">需求</span><span class="sxs-lookup"><span data-stu-id="341fa-118">Requirement</span></span> | <span data-ttu-id="341fa-119">值</span><span class="sxs-lookup"><span data-stu-id="341fa-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="341fa-120">標頭</span><span class="sxs-lookup"><span data-stu-id="341fa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="341fa-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="341fa-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="341fa-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="341fa-122">Library</span></span><br/> | <dl> <span data-ttu-id="341fa-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="341fa-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="341fa-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="341fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341fa-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="341fa-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="341fa-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="341fa-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




