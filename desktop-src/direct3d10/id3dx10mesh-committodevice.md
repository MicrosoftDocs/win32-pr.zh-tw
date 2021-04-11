---
description: 將對網格所做的任何變更認可到裝置，以便轉譯變更。 這應該在網格的資料改變之後，以及轉譯之前呼叫。 除非已對裝置認可網狀，否則無法轉譯。 請參閱＜備註＞。
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh：： CommitToDevice 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035360"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="ccde4-106">ID3DX10Mesh：： CommitToDevice 方法</span><span class="sxs-lookup"><span data-stu-id="ccde4-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="ccde4-107">將對網格所做的任何變更認可到裝置，以便轉譯變更。</span><span class="sxs-lookup"><span data-stu-id="ccde4-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="ccde4-108">這應該在網格的資料改變之後，以及轉譯之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="ccde4-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="ccde4-109">除非已對裝置認可網狀，否則無法轉譯。</span><span class="sxs-lookup"><span data-stu-id="ccde4-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="ccde4-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ccde4-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccde4-111">語法</span><span class="sxs-lookup"><span data-stu-id="ccde4-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="ccde4-112">參數</span><span class="sxs-lookup"><span data-stu-id="ccde4-112">Parameters</span></span>

<span data-ttu-id="ccde4-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ccde4-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ccde4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccde4-114">Return value</span></span>

<span data-ttu-id="ccde4-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccde4-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccde4-116">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ccde4-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccde4-117">備註</span><span class="sxs-lookup"><span data-stu-id="ccde4-117">Remarks</span></span>

<span data-ttu-id="ccde4-118">當網格載入時，就會將它的資料載入預備資源，這表示資料可以改變但無法轉譯。</span><span class="sxs-lookup"><span data-stu-id="ccde4-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="ccde4-119">呼叫 CommitToDevice 時，會將來自預備資源的資料複製到裝置資源，以便轉譯。</span><span class="sxs-lookup"><span data-stu-id="ccde4-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="ccde4-120">雖然資料會認可至裝置，但暫存資源仍可供修改。</span><span class="sxs-lookup"><span data-stu-id="ccde4-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="ccde4-121">如果對預備資源進行任何修改，則必須再次將預備資源認可至裝置，才能在螢幕上轉譯這些變更。</span><span class="sxs-lookup"><span data-stu-id="ccde4-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccde4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccde4-122">Requirements</span></span>



| <span data-ttu-id="ccde4-123">需求</span><span class="sxs-lookup"><span data-stu-id="ccde4-123">Requirement</span></span> | <span data-ttu-id="ccde4-124">值</span><span class="sxs-lookup"><span data-stu-id="ccde4-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccde4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ccde4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ccde4-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccde4-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccde4-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ccde4-127">Library</span></span><br/> | <dl> <span data-ttu-id="ccde4-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccde4-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccde4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccde4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccde4-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ccde4-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ccde4-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ccde4-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




