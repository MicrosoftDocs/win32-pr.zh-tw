---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: 'IDWriteBitmapRenderTarget2 (dwrite_3 .h) '
description: 封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195687"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>IDWriteBitmapRenderTarget2 介面 (dwrite_3 .h) 

封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。

> [!IMPORTANT]
> 此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。 DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。 如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview)。

## <a name="inheritance"></a>繼承

**IDWriteBitmapRenderTarget2** 介面繼承自 [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)。

## <a name="methods"></a>方法

**IDWriteBitmapRenderTarget2** 介面具有這些方法。

| 方法 | 描述 |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2::GetBitmapData](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | 從點陣圖呈現目標抓取圖元資料。 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，Project 留尼旺島0.1 發行前版本 [Win32 應用程式] |
| **標頭** | dwrite_3 .h (包含 dwrite_core .h)  |