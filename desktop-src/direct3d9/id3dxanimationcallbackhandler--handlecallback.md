---
description: 應用程式會執行此方法。 呼叫 ID3DXAnimationController：： AdvanceTime 期間，在其中一個追蹤中設定動畫的回呼時，會呼叫這個方法。
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler：： HandleCallback 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976520"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="0178c-104">ID3DXAnimationCallbackHandler：： HandleCallback 方法</span><span class="sxs-lookup"><span data-stu-id="0178c-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="0178c-105">應用程式會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="0178c-105">The application implements this method.</span></span> <span data-ttu-id="0178c-106">呼叫 [**ID3DXAnimationController：： AdvanceTime**](id3dxanimationcontroller--advancetime.md)期間，在其中一個追蹤中設定動畫的回呼時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0178c-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0178c-107">語法</span><span class="sxs-lookup"><span data-stu-id="0178c-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="0178c-108">參數</span><span class="sxs-lookup"><span data-stu-id="0178c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0178c-109">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0178c-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0178c-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0178c-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0178c-111">回呼發生所在之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0178c-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="0178c-112">*pCallbackData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0178c-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0178c-113">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0178c-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0178c-114">使用者擁有的回呼資料指標。</span><span class="sxs-lookup"><span data-stu-id="0178c-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0178c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0178c-115">Return value</span></span>

<span data-ttu-id="0178c-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0178c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0178c-117">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="0178c-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0178c-118">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0178c-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0178c-119">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="0178c-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0178c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0178c-120">Requirements</span></span>



| <span data-ttu-id="0178c-121">需求</span><span class="sxs-lookup"><span data-stu-id="0178c-121">Requirement</span></span> | <span data-ttu-id="0178c-122">值</span><span class="sxs-lookup"><span data-stu-id="0178c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0178c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0178c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0178c-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="0178c-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0178c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="0178c-125">Library</span></span><br/> | <dl> <span data-ttu-id="0178c-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0178c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0178c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0178c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0178c-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="0178c-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
