---
description: 下表包含 API 函數的傳回碼。
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Direct3D 10 傳回碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c7e7bca25d240bf7775a6f4d6476148e3749e283ab4f8fb3511bf8b53bb711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282798"
---
# <a name="direct3d-10-return-codes"></a>Direct3D 10 傳回碼

下表包含 API 函數的傳回碼。



| HRESULT                                         | 描述                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 找不到 D3D10 錯誤檔案                  | 找不到檔案。                                                                                                                               |
| D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件 | 特定類型之 [狀態物件](d3d10-graphics-programming-guide-api-features-state-objects.md)的唯一實例太多。          |
| D3DERR \_ INVALIDCALL                             | 方法呼叫無效。 例如，方法的參數可能不是有效的指標。                                                             |
| D3DERR \_ WASSTILLDRAWING                         | 先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。                                                   |
| E \_ 失敗                                         | 嘗試建立啟用了 [debug 層](d3d10-graphics-programming-guide-api-features-layers.md) 的裝置，且未安裝該層。 |
| E \_ INVALIDARG                                   | 傳遞了不正確參數給傳回的函式。                                                                                            |
| E \_ OUTOFMEMORY                                  | Direct3D 無法配置足夠的記憶體來完成呼叫。                                                                                   |
| E \_ >NOTIMPL                                      | 未以傳遞的參數組合來執行方法呼叫。                                                                              |
| S \_ FALSE                                        | 替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。                                 |
| S \_ 確定                                           | 未發生任何錯誤。                                                                                                                                    |



 

若要撰寫可妥善處理 [HRESULT 值](../winprog/windows-data-types.md) 的程式碼，請使用成功的 (hr) 和失敗 (hr) 宏。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 參考](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Direct3D 10 的參考](d3d10-graphics-reference.md)
</dt> </dl>

 

 
