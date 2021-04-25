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
ms.openlocfilehash: f84959338550722d9ce1d2d7097d652fcb140f1f
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955041"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>IDWriteBitmapRenderTarget2：： GetBitmapData 方法 (dwrite_3 .h) 

從點陣圖呈現目標抓取圖元資料。

> [!IMPORTANT]
> 此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。 DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。 如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview)。

## <a name="syntax"></a>語法

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>參數

`bitmapData`

輸入： \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

圖元資料的指標。

## <a name="return-value"></a>傳回值

類型： <b>HRESULT</b>

如果這個方法成功，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>。 否則，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> 錯誤碼。

## <a name="examples"></a>範例

請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，專案留尼旺島 [Win32 apps] |
| **標頭** | dwrite_3 .h (包含 dwrite_core .h)  |
| **程式庫** | Dwrite .lib |
| **DLL** | Dwrite.dll |

## <a name="see-also"></a>另請參閱

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
