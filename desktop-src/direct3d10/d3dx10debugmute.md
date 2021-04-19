---
description: 啟用或停用 debug 訊息。
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: 'D3DX10DebugMute 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989213"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="51eea-103">D3DX10DebugMute 函式</span><span class="sxs-lookup"><span data-stu-id="51eea-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="51eea-104">啟用或停用 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="51eea-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="51eea-105">語法</span><span class="sxs-lookup"><span data-stu-id="51eea-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="51eea-106">參數</span><span class="sxs-lookup"><span data-stu-id="51eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51eea-107">*靜音* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51eea-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51eea-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51eea-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51eea-109">設定為 **TRUE** 以啟用 debug 訊息;設定為 **FALSE** 以停用 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="51eea-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51eea-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="51eea-110">Return value</span></span>

<span data-ttu-id="51eea-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="51eea-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="51eea-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="51eea-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="51eea-113">備註</span><span class="sxs-lookup"><span data-stu-id="51eea-113">Remarks</span></span>

<span data-ttu-id="51eea-114">使用此函式可在 debug 期間停用 D3DX10 Api 的錯誤訊息;使用此函式應該受到 D3D10 \_ DEBUG 編譯器參數的保護。</span><span class="sxs-lookup"><span data-stu-id="51eea-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="51eea-115">Debug 組建的預設狀態為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="51eea-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="51eea-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="51eea-116">Requirements</span></span>



| <span data-ttu-id="51eea-117">需求</span><span class="sxs-lookup"><span data-stu-id="51eea-117">Requirement</span></span> | <span data-ttu-id="51eea-118">值</span><span class="sxs-lookup"><span data-stu-id="51eea-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51eea-119">標頭</span><span class="sxs-lookup"><span data-stu-id="51eea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="51eea-120"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="51eea-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="51eea-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="51eea-121">Library</span></span><br/> | <dl> <span data-ttu-id="51eea-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="51eea-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51eea-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51eea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51eea-124">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="51eea-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
