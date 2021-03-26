---
UID: ''
title: SHIsChildOrSelf 函式
description: 比較視窗是否等於第二個視窗的子系、的子系或子代。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104990875"
---
# <a name="shischildorself-function"></a><span data-ttu-id="c0454-103">SHIsChildOrSelf 函式</span><span class="sxs-lookup"><span data-stu-id="c0454-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="c0454-104">Description</span><span class="sxs-lookup"><span data-stu-id="c0454-104">Description</span></span>

<span data-ttu-id="c0454-105">\[這項功能可透過 Windows XP 和 Windows Server 2003 取得。</span><span class="sxs-lookup"><span data-stu-id="c0454-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="c0454-106">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c0454-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c0454-107">比較視窗是否等於第二個視窗的子系、的子系或子代。</span><span class="sxs-lookup"><span data-stu-id="c0454-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="c0454-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0454-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="c0454-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="c0454-109">hwndParent [in]</span></span>

<span data-ttu-id="c0454-110">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="c0454-110">Type: **HWND**</span></span>

<span data-ttu-id="c0454-111">第一個視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0454-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="c0454-112">hwnd [in]</span><span class="sxs-lookup"><span data-stu-id="c0454-112">hwnd [in]</span></span>

<span data-ttu-id="c0454-113">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="c0454-113">Type: **HWND**</span></span>

<span data-ttu-id="c0454-114">要針對 *hwndParent* 進行測試的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0454-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="c0454-115">傳回</span><span class="sxs-lookup"><span data-stu-id="c0454-115">Returns</span></span>

<span data-ttu-id="c0454-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c0454-116">Type: **HRESULT**</span></span>

<span data-ttu-id="c0454-117">如果 *hwnd* 指定的視窗等於、的子系或 *hwndParent* 所指定視窗的子系，則會傳回 **S_OK** 。</span><span class="sxs-lookup"><span data-stu-id="c0454-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="c0454-118">如果 hwnd 指定的視窗不等於、非的子系，而不是 *hwndParent* 所指定視窗的子系，則會傳回 **S_FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c0454-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="c0454-119">如果任一視窗控制碼無效，則傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="c0454-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0454-120">備註</span><span class="sxs-lookup"><span data-stu-id="c0454-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="c0454-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0454-121">See also</span></span>

[<span data-ttu-id="c0454-122">IsChild</span><span class="sxs-lookup"><span data-stu-id="c0454-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
