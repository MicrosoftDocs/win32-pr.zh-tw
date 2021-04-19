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
ms.openlocfilehash: ea60bbd4933cd890321e0caeb095778922699a46
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106975586"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>DWRITE_BITMAP_DATA_BGRA32 結構 (dwrite_3 .h) 

代表 BGRA32 格式的點陣圖資料。

> [!IMPORTANT]
> 此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。 DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。 如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview)。

## <a name="syntax"></a>語法

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>成員

`width`

類型： **[UINT32](../../winprog/windows-data-types.md)**

點陣圖的寬度（以圖元為單位）。


`height`

類型： **[UINT32](../../winprog/windows-data-types.md)**

點陣圖的高度（以圖元為單位）。


`pixels`

類型： \_ 欄位 \_ 大小 \_ (寬度 * 高度) **[UINT32](../../winprog/windows-data-types.md)\***

點陣圖位值位置的指標。


## <a name="examples"></a>範例

請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，Project 留尼旺島0.1 發行前版本 [Win32 應用程式] |
| **標頭** | dwrite_3 .h (包含 dwrite_core .h)  |