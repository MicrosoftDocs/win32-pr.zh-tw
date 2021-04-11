---
description: Direct3D 裝置可能在操作狀態或遺失狀態。
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: " (Direct3D 9) 的裝置遺失"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317708"
---
# <a name="lost-devices-direct3d-9"></a> (Direct3D 9) 的裝置遺失

Direct3D 裝置可能在操作狀態或遺失狀態。 操作狀態是一般裝置狀態，裝置如預期般執行和呈現所有轉譯。 該裝置會轉換成遺失狀態，例如在全螢幕應用程式中遺失鍵盤焦點，會導致不可能轉譯。 遺失狀態的特性所有轉譯操作無聲息地失敗，這表示轉譯方法可傳回成功碼，即使所有的轉譯作業失敗。 在此情況下， \_ IDirect3DDevice9 會傳回錯誤碼 D3DERR DEVICELOST [**：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送。

經過設計，未指定可能會導致裝置遺失的整套案例。 一些常見的範例包括焦點，例如當使用者按下 ALT + TAB 或當初始化系統對話方塊時。 裝置也可能因電源管理事件而遺失，或在另一個應用程式繼續全螢幕作業時遺失。 此外， [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 的任何失敗都會使裝置處於遺失狀態。

所有衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)的方法，保證在裝置遺失之後運作。 遺失裝置之後，每項功能通常具有以下三個選項︰

-   使用 D3DERR \_ DEVICELOST 失敗-這表示應用程式必須辨識裝置已遺失，如此應用程式才能識別出未如預期般發生的問題。
-   以無訊息方式失敗、傳回 S \_ 確定或任何其他傳回碼-如果函式以無訊息模式失敗，應用程式通常無法區分「成功」和「無提示失敗」的結果。
-   函數會傳回傳回碼。



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> Direct3D 9 裝置會傳回 D3DERR \_ DEVICELOST。 從 IDirect3DDevice9 傳回之後 [**：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送，模擬行為不再運作，而且未來的所有呼叫都會失敗，直到成功重設裝置為止。<br/> Direct3D 9Ex 裝置絕不會傳回 D3DERR \_ DEVICELOST，但可以傳回新的狀態訊息， (查看 [裝置行為變更](dx9lh.md)) 。<br/> |



 

## <a name="responding-to-a-lost-device"></a>回應遺失裝置

遺失的裝置必須在重設後重新建立資源 (包括視訊記憶體資源)。 如果遺失裝置，應用程式會查詢裝置，查看是否可以還原到運作狀態。 若否，應用程式會等到裝置還原。

如果可以還原裝置，應用程式會藉由破壞所有影片記憶體資源和任何交換鏈來準備裝置。 然後，應用程式會呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 方法。 Reset 是唯一會在裝置遺失時生效的方法，而是應用程式可以將裝置從遺失變成操作狀態的唯一方法。 除非應用程式釋放 D3DPOOL 預設中所配置的所有資源 \_ （包括由 [**IDirect3DDevice9：： CreateRenderTarget**](/windows/desktop/api) 和 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) 方法建立的資源），否則重設將會失敗。

大部分的 Direct3D 高頻呼叫不會傳回是否裝置已遺失的任何資訊。 應用程式可繼續呼叫轉譯方法（例如 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)），而不會收到遺失裝置的通知。 內部將會捨棄這些作業，直到裝置重設為操作狀態。

應用程式可以藉由查詢 [**IDirect3DDevice9：： TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) 方法的傳回值，來判斷遇到遺失裝置時要採取的動作。

## <a name="locking-operations"></a>鎖定作業

在內部 Direct3D 運作以確保遺失裝置之後成功鎖定作業。 不過，它並不保證鎖定作業期間影片記憶體資源的資料是準確的。 它保證不傳回錯誤碼。 這可讓應用程式寫入，不需擔心鎖定作業期間遺失裝置。

## <a name="resources"></a>資源

資源可能會消耗視訊記憶體。 遺失的裝置與介面卡擁有的視訊記憶體中斷連線，所以不保證遺失裝置時的視訊記憶體配置。 如此一來，所有資源建立方法都可以藉由傳回 D3D OK 來成功完成 \_ ，但實際上只會配置虛擬系統記憶體。 必須先破壞任何視訊記憶體資源，再重新調整裝置大小，如此就不會有過度配置視訊記憶體的問題。 這些虛擬表面可讓鎖定和複製作業正常運作，直到應用程式呼叫 [**IDirect3DDevice9 為止：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送併發現裝置已遺失。

必須發佈所有的視訊記憶體，才能將裝置從遺失狀態重設為可操作狀態。 這表示應用程式應該釋放以 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 建立的任何交換鏈，以及放在 D3DPOOL 預設記憶體類別中的任何資源 \_ 。 應用程式不需要釋放 D3DPOOL \_ MANAGED 或 D3DPOOL \_ SYSTEMMEM 記憶體類別中的資源。 在轉換到操作狀態時，其他狀態資料會自動損壞。

您可以使用單一程式碼路徑開發應用程式，以回應裝置遺失。 此程式碼路徑如果和初始啟動裝置的程式碼路徑不相同，也會很類似。

## <a name="retrieved-data"></a>擷取的資料

Direct3D 可讓應用程式使用 [**IDirect3DDevice9：： ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice)來驗證硬體的材質和轉譯狀態。 此方法通常會在應用程式初始化期間叫用，如果裝置已遺失，則會傳回 D3DERR \_ DEVICELOST。

Direct3D 也可讓應用程式複製已產生或先前從視訊記憶體資源寫入影像至非揮發性系統記憶體資源。 這類傳輸的來源影像可能隨時會遺失，因此 Direct3D 允許在裝置遺失讓此類複製作業失敗。

關於非同步查詢， [**IDirect3DQuery9：：：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) D3DERR 會傳回 \_ DEVICELOST （如果已指定 FLUSH 旗標），以向應用程式指出 **IDirect3DQuery9：：** 絕不會傳回 S \_ OK。

複製作業（ [**IDirect3DDevice9：： GetFrontBufferData**](/windows/desktop/api)）可能會因為 D3DERR DEVICELOST 而失敗， \_ 因為裝置遺失時，沒有主要介面。 [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 也可能會因為 D3DERR DEVICELOST 而失敗， \_ 因為當裝置遺失時，無法建立背景緩衝區。 請注意，這些案例是 IDirect3DDevice9 以外的唯一 D3DERR \_ DEVICELOST 實例 [**：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送、 [**IDirect3DDevice9：： TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)和 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 方法。

## <a name="programmable-shaders"></a>可程式化著色器

在 Direct3D 9 中，重設之後不需要重新建立頂點著色器和圖元著色器。 系統會記住它們。 在舊版的 DirectX 中，遺失的裝置需要重新建立著色器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
