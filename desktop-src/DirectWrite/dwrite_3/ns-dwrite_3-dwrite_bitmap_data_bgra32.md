---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: 'DWRITE_BITMAP_DATA_BGRA32 (dwrite_3 .h) '
description: 代表 BGRA32 格式的點陣圖資料。
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955051"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="727fb-103">DWRITE_BITMAP_DATA_BGRA32 結構 (dwrite_3 .h) </span><span class="sxs-lookup"><span data-stu-id="727fb-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="727fb-104">代表 BGRA32 格式的點陣圖資料。</span><span class="sxs-lookup"><span data-stu-id="727fb-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="727fb-105">此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="727fb-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="727fb-106">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="727fb-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="727fb-107">如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview)。</span><span class="sxs-lookup"><span data-stu-id="727fb-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="727fb-108">語法</span><span class="sxs-lookup"><span data-stu-id="727fb-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="727fb-109">成員</span><span class="sxs-lookup"><span data-stu-id="727fb-109">Members</span></span>

`width`

<span data-ttu-id="727fb-110">類型： **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="727fb-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="727fb-111">點陣圖的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="727fb-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="727fb-112">類型： **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="727fb-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="727fb-113">點陣圖的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="727fb-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="727fb-114">類型： \_ 欄位 \_ 大小 \_ (寬度 \* 高度) **[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="727fb-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="727fb-115">點陣圖位值位置的指標。</span><span class="sxs-lookup"><span data-stu-id="727fb-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="727fb-116">範例</span><span class="sxs-lookup"><span data-stu-id="727fb-116">Examples</span></span>

<span data-ttu-id="727fb-117">請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="727fb-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="727fb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="727fb-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="727fb-119">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="727fb-119">**Minimum supported client**</span></span> | <span data-ttu-id="727fb-120">Windows 10，專案留尼旺島 [Win32 apps]</span><span class="sxs-lookup"><span data-stu-id="727fb-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="727fb-121">**標頭**</span><span class="sxs-lookup"><span data-stu-id="727fb-121">**Header**</span></span> | <span data-ttu-id="727fb-122">dwrite_3 .h (包含 dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="727fb-122">dwrite_3.h (include dwrite_core.h)</span></span> |