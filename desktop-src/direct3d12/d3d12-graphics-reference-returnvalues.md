---
title: Direct3D 12 傳回碼
description: 以下是來自 API 函數的傳回碼。
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968298"
---
# <a name="direct3d-12-return-codes"></a>Direct3D 12 傳回碼

以下是來自 API 函數的傳回碼。 如需傳回碼的詳細資訊，請參閱 [DXGI \_ 錯誤](/windows/desktop/direct3ddxgi/dxgi-error)。



| HRESULT                                                                  | Description                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ 找不到 D3D12 錯誤介面卡 \_                                        | 指定的快取 PSO 是在不同的介面卡上建立的，無法在目前的介面卡上重複使用。          |
| D3D12 \_ 錯誤 \_ 驅動程式 \_ 版本 \_ 不符                                  | 指定的快取 PSO 是在不同的驅動程式版本上建立的，無法在目前的介面卡上重複使用。  |
| D3DERR \_ INVALIDCALL (取代了 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫)            | 方法呼叫無效。 例如，方法的參數可能不是有效的指標。                             |
| D3DERR \_ WASSTILLDRAWING (取代了 DXGI \_ 錯誤 \_ ， \_ 仍在 \_ 繪圖中)  | 先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。                   |
| E \_ 失敗                                                                  | 嘗試建立啟用了 debug 層的裝置，且未安裝該層。                             |
| E \_ INVALIDARG                                                            | 傳遞了不正確參數給傳回的函式。                                                             |
| E \_ OUTOFMEMORY                                                           | Direct3D 無法配置足夠的記憶體來完成呼叫。                                                   |
| E \_ >NOTIMPL                                                               | 未以傳遞的參數組合來執行方法呼叫。                                               |
| S \_ FALSE                                                                 | 替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。 |
| S \_ 確定                                                                    | 未發生任何錯誤。                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> </dl>

 

 