---
description: 在 Direct3D 9 中，Direct3D 可讓驅動程式傳回錯誤碼（例如 E \_ OUTOFMEMORY、D3DERR \_ OUTOFVIDEOMEMORY 和 D3DERR UNSUPPORTEDCOLORARG）， \_ 讓應用程式能夠回應這些錯誤碼。
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: " (Direct3D 9) 的驅動程式內部錯誤"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109341"
---
# <a name="driver-internal-errors-direct3d-9"></a> (Direct3D 9) 的驅動程式內部錯誤

在 Direct3D 9 中，Direct3D 可讓驅動程式傳回錯誤碼（例如 E \_ OUTOFMEMORY、D3DERR \_ OUTOFVIDEOMEMORY 和 D3DERR UNSUPPORTEDCOLORARG）， \_ 讓應用程式能夠回應這些錯誤碼。 不過，有時產生這些傳回型別的 API 呼叫會載入至命令緩衝區，並進行批次處理以傳送至 GPU (請參閱 [控制執行時間和驅動程式優化](accurately-profiling-direct3d-api-calls.md)) 。 在此情況下，當需要採取動作時，錯誤無法轉送至應用程式，因此執行時間會取用錯誤碼，並在發生這種情況時對裝置物件發出附注。 稍後當應用程式叫用 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送時， **IDirect3DDevice9：:P** 重新傳送將會傳回 D3DERR \_ DRIVERINTERNALERROR。 這就是為什麼當應用程式收到來自 IDirect3DDevice9 的 D3DERR DRIVERINTERNALERROR 時，應用程式的最佳方法 \_ **：:P** 重新傳送是終結並重新建立裝置。

如果您想要進一步進行偵錯工具，以下有幾個建議您嘗試找出產生錯誤的 API 呼叫：

-   因為可能傳回值的清單不完整，所以您可以嘗試找出每個 API 呼叫的周圍失敗的呼叫，如下所示：

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    輸出的 debug 資料流程應該會顯示造成此問題的呼叫。

-   此外，基於偵錯工具的目的，請嘗試在每個 IDirect3DDevice9 之前立即呼叫 [**IDirect3DDevice9：： ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) [**：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 以查看設備磁碟機是否有額外的問題 (不支援的作業、材質格式的組合等) 。

    > [!Note]  
    > [**IDirect3DDevice9：： ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) 應該謹慎地使用，因為驅動程式必須執行的驗證工作量，才能傳回答案。

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計秘訣](programming-tips.md)
</dt> </dl>

 

 
