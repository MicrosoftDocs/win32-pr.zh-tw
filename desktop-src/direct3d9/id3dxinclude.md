---
description: ID3DXInclude 是使用者執行的介面，可為 \# 著色器編譯期間的 include 指示詞提供回呼。
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: 'ID3DXInclude 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991494"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="e3e3b-103">ID3DXInclude 介面</span><span class="sxs-lookup"><span data-stu-id="e3e3b-103">ID3DXInclude interface</span></span>

<span data-ttu-id="e3e3b-104">ID3DXInclude 是使用者執行的介面，可為 \# 著色器編譯期間的 include 指示詞提供回呼。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="e3e3b-105">這個介面中的每個方法都必須由使用者執行，當發生下列其中一種情況時，就會用來做為應用程式的回呼：</span><span class="sxs-lookup"><span data-stu-id="e3e3b-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="e3e3b-106">包含包含的 HLSL 著色器 \# 會藉由呼叫其中一個 D3DXCompileShader 函數來進行編譯 \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e3e3b-107">元件著色器 \# 包含的組合是藉由呼叫任何 D3DXAssembleShader \* \* \* 函數。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e3e3b-108">包含包含的效果 \# 會藉由呼叫任何 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數來編譯。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="e3e3b-109">成員</span><span class="sxs-lookup"><span data-stu-id="e3e3b-109">Members</span></span>

<span data-ttu-id="e3e3b-110">**ID3DXInclude** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e3e3b-111">**ID3DXInclude** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e3e3b-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="e3e3b-112">方法</span><span class="sxs-lookup"><span data-stu-id="e3e3b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e3e3b-113">方法</span><span class="sxs-lookup"><span data-stu-id="e3e3b-113">Methods</span></span>

<span data-ttu-id="e3e3b-114">**ID3DXInclude** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="e3e3b-115">方法</span><span class="sxs-lookup"><span data-stu-id="e3e3b-115">Method</span></span>                               | <span data-ttu-id="e3e3b-116">描述</span><span class="sxs-lookup"><span data-stu-id="e3e3b-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3e3b-117">**關閉**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="e3e3b-118">使用者執行的方法，用於關閉著色器的 \# 包含檔案。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="e3e3b-119">**打開**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="e3e3b-120">使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3e3b-121">備註</span><span class="sxs-lookup"><span data-stu-id="e3e3b-121">Remarks</span></span>

<span data-ttu-id="e3e3b-122">使用者藉由實作為衍生自這個介面的類別，以及執行所有介面方法，來建立 ID3DXInclude 介面。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="e3e3b-123">LPD3DXINCLUDE 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e3e3b-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="e3e3b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3e3b-124">Requirements</span></span>



| <span data-ttu-id="e3e3b-125">需求</span><span class="sxs-lookup"><span data-stu-id="e3e3b-125">Requirement</span></span> | <span data-ttu-id="e3e3b-126">值</span><span class="sxs-lookup"><span data-stu-id="e3e3b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e3b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e3e3b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e3e3b-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e3b-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e3e3b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3e3b-129">Library</span></span><br/> | <dl> <span data-ttu-id="e3e3b-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3e3b-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e3e3b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3e3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e3b-132">效果介面</span><span class="sxs-lookup"><span data-stu-id="e3e3b-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
