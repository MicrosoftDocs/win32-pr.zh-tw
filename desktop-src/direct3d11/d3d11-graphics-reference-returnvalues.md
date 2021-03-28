---
title: Direct3D 11 傳回碼
description: API 函數的傳回碼。
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4130ed07faaabfd24bb48454d4e450f307c7a12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023613"
---
# <a name="direct3d-11-return-codes"></a>Direct3D 11 傳回碼

從 API 函式傳回碼。

| HRESULT | Description |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002)  | 找不到檔案。 |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001)  | 特定類型之狀態物件的唯一實例太多。 |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003)  | 特定類型之 view 物件的唯一實例太多。 |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004)  | 不 D3D11_MAP_WRITE_DISCARD 每個資源的 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)或 [**>id3d11devicecoNtext：： FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist)之後第一次呼叫 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 。 |
| D3DERR_INVALIDCALL (取代為 DXGI_ERROR_INVALID_CALL)  (0x887A0001)  | 方法呼叫無效。 例如，方法的參數可能不是有效的指標。 |
| D3DERR_WASSTILLDRAWING (取代為 DXGI_ERROR_WAS_STILL_DRAWING)  (0x887A000A)  | 先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。 |
| E_FAIL (0x80004005) | 嘗試建立啟用了 debug 層的裝置，且未安裝該層。 |
| E_INVALIDARG (0x80070057)  | 傳遞了不正確參數給傳回的函式。 |
| E_OUTOFMEMORY (0x8007000E)  | Direct3D 無法配置足夠的記憶體來完成呼叫。 |
| E_NOTIMPL (0x80004001)  | 未以傳遞的參數組合來執行方法呼叫。 |
| S_FALSE ( (HRESULT) 1L)  | 替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。 |
| S_OK ( (HRESULT) 0L)  | 未發生任何錯誤。 |

如需傳回碼的詳細資訊，請參閱 [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error)。

## <a name="related-topics"></a>相關主題

* [Direct3D 11 參考](d3d11-graphics-reference.md)