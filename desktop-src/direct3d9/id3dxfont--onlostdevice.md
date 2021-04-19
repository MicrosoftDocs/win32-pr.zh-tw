---
description: 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'ID3DXFont：： OnLostDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000604"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="f904f-104">ID3DXFont：： OnLostDevice 方法</span><span class="sxs-lookup"><span data-stu-id="f904f-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="f904f-105">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="f904f-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="f904f-106">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f904f-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f904f-107">語法</span><span class="sxs-lookup"><span data-stu-id="f904f-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="f904f-108">參數</span><span class="sxs-lookup"><span data-stu-id="f904f-108">Parameters</span></span>

<span data-ttu-id="f904f-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f904f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f904f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f904f-110">Return value</span></span>

<span data-ttu-id="f904f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f904f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f904f-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f904f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f904f-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f904f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f904f-114">備註</span><span class="sxs-lookup"><span data-stu-id="f904f-114">Remarks</span></span>

<span data-ttu-id="f904f-115">只要裝置遺失或使用者呼叫 [**重設**](/windows/desktop/api)之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f904f-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="f904f-116">即使裝置實際上未遺失， **OnLostDevice** 仍負責釋放 stateblocks 和其他可能需要先釋出才能重設裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f904f-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="f904f-117">如此一來，在呼叫 **Reset** 然後 [**OnResetDevice**](id3dxfont--onresetdevice.md)之前，無法再次使用字型物件。</span><span class="sxs-lookup"><span data-stu-id="f904f-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f904f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f904f-118">Requirements</span></span>



| <span data-ttu-id="f904f-119">需求</span><span class="sxs-lookup"><span data-stu-id="f904f-119">Requirement</span></span> | <span data-ttu-id="f904f-120">值</span><span class="sxs-lookup"><span data-stu-id="f904f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f904f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f904f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f904f-122"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="f904f-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f904f-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f904f-123">Library</span></span><br/> | <dl> <span data-ttu-id="f904f-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f904f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f904f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f904f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f904f-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="f904f-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




