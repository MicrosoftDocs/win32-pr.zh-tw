---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: 'IDWriteBitmapRenderTarget2：： GetBitmapData (dwrite_3 .h) '
description: 從點陣圖呈現目標抓取圖元資料。
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550283"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="dbe4b-103">IDWriteBitmapRenderTarget2：： GetBitmapData 方法 (dwrite_3 .h) </span><span class="sxs-lookup"><span data-stu-id="dbe4b-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="dbe4b-104">從點陣圖呈現目標抓取圖元資料。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbe4b-105">此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="dbe4b-106">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="dbe4b-107">如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](../dwritecore-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe4b-108">語法</span><span class="sxs-lookup"><span data-stu-id="dbe4b-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="dbe4b-109">參數</span><span class="sxs-lookup"><span data-stu-id="dbe4b-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="dbe4b-110">輸入： \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbe4b-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="dbe4b-111">圖元資料的指標。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbe4b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbe4b-112">Return value</span></span>

<span data-ttu-id="dbe4b-113">類型： <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="dbe4b-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="dbe4b-114">如果這個方法成功，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="dbe4b-115">否則，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="dbe4b-116">範例</span><span class="sxs-lookup"><span data-stu-id="dbe4b-116">Examples</span></span>

<span data-ttu-id="dbe4b-117">請參閱 [DWriteCore 總覽](../dwritecore-overview.md) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="dbe4b-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe4b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbe4b-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dbe4b-119">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="dbe4b-119">**Minimum supported client**</span></span> | <span data-ttu-id="dbe4b-120">Windows 10，專案留尼旺島 [Win32 apps]</span><span class="sxs-lookup"><span data-stu-id="dbe4b-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="dbe4b-121">**標頭**</span><span class="sxs-lookup"><span data-stu-id="dbe4b-121">**Header**</span></span> | <span data-ttu-id="dbe4b-122">dwrite_3 .h (包含 dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="dbe4b-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="dbe4b-123">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="dbe4b-123">**Library**</span></span> | <span data-ttu-id="dbe4b-124">Dwrite .lib</span><span class="sxs-lookup"><span data-stu-id="dbe4b-124">Dwrite.lib</span></span> |
| <span data-ttu-id="dbe4b-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="dbe4b-125">**DLL**</span></span> | <span data-ttu-id="dbe4b-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="dbe4b-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="dbe4b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe4b-127">See also</span></span>

[<span data-ttu-id="dbe4b-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="dbe4b-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)