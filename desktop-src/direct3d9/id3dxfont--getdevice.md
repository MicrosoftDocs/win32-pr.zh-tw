---
description: 抓取與字型物件相關聯的 Direct3D 裝置。
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'ID3DXFont：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323319"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="13058-103">ID3DXFont：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="13058-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="13058-104">抓取與字型物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="13058-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13058-105">語法</span><span class="sxs-lookup"><span data-stu-id="13058-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="13058-106">參數</span><span class="sxs-lookup"><span data-stu-id="13058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13058-107">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13058-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13058-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="13058-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="13058-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與字型物件相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="13058-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13058-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="13058-110">Return value</span></span>

<span data-ttu-id="13058-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13058-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13058-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="13058-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="13058-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="13058-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="13058-114">備註</span><span class="sxs-lookup"><span data-stu-id="13058-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="13058-115">呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="13058-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="13058-116">當您使用這個 **IDirect3DDevice9** 介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="13058-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13058-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="13058-117">Requirements</span></span>



| <span data-ttu-id="13058-118">需求</span><span class="sxs-lookup"><span data-stu-id="13058-118">Requirement</span></span> | <span data-ttu-id="13058-119">值</span><span class="sxs-lookup"><span data-stu-id="13058-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13058-120">標頭</span><span class="sxs-lookup"><span data-stu-id="13058-120">Header</span></span><br/>  | <dl> <span data-ttu-id="13058-121"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="13058-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="13058-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="13058-122">Library</span></span><br/> | <dl> <span data-ttu-id="13058-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13058-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13058-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13058-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13058-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="13058-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
