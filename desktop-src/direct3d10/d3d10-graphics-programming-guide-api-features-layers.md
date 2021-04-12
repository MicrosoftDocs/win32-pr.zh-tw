---
description: " (Direct3D 10) 的 API 層"
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: " (Direct3D 10) 的 API 層"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427083bdcaf389c4b01b590a1bc3fef7eb878b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385892"
---
# <a name="api-layers-direct3d-10"></a> (Direct3D 10) 的 API 層

Direct3D 10 執行時間是以核心的基本功能為基礎，並在外部層建立選擇性和開發人員輔助的功能，並以層級進行。

## <a name="core-layer"></a>核心層

核心層預設為存在;在 API 和設備磁碟機之間提供非常精簡的對應，將高頻率呼叫的額外負荷降至最低。 因為核心層是效能不可或缺的，所以它只會執行重大驗證。

其餘層是選擇性的。 一般來說，圖層會加入功能，但不會修改現有的行為。 例如，除了要具現化的調試層之外，核心函式的傳回值也會與所具現化的調試層有相同的傳回值。

藉由呼叫 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) 並提供一或多個 [**D3D10 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) 標值來建立裝置時，請建立圖層。

## <a name="debug-layer"></a>Debug 圖層

Debug 層提供大量的額外參數和一致性驗證 (例如驗證著色器連結和資源系結、驗證參數一致性，以及報告錯誤描述) 。 Debug 層所產生的輸出包含可使用 [**ID3D10InfoQueue 介面**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) 存取的字串佇列 (請參閱 [使用 ID3D10InfoQueue (Direct3D 10) ) 自訂偵錯工具輸出](d3d10-graphics-programming-guide-api-features-layers-info-queue.md) 。 核心層產生的錯誤會以調試層的警告反白顯示。

若要建立支援 debug 層的裝置，您必須安裝 DirectX SDK (才能取得 D3D10SDKLayers.DLL) ，然後在 \_ \_ \_ 呼叫 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)時指定 D3D10 建立裝置的偵錯工具旗標。 當然，使用 debug 層執行應用程式的速度將會大幅降低。 若要啟用/停用 D3DX10 Api 的偵錯工具訊息，請呼叫 [**D3DX10DebugMute**](d3dx10debugmute.md)。

當 debug 圖層列出記憶體流失時，它會輸出物件介面指標清單及其易記名稱。 預設的易記名稱是「 &lt; 未命名」 &gt; 。 您可以使用 [**ID3D10DeviceChild：： SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) 方法以及 D3Dcommon 中的 **WKPDID \_ D3DDebugObjectName** GUID 來設定易記名稱。 例如，若要以 SDKLayer 名稱 mytexture.jpg 命名 pTexture，請使用下列程式碼：


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



一般而言，您應該從生產版本編譯這些呼叫。

## <a name="switch-to-reference-layer"></a>切換至參考圖層

這一層可讓應用程式在硬體裝置 (HAL) 和參照或軟體裝置 (REF) 之間進行轉換。 若要切換裝置，您必須先建立支援切換至參考層的裝置 (請參閱 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) ，然後呼叫 [**ID3D10SwitchToRef：： SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref)。

所有裝置狀態、資源和物件都會透過此裝置轉換進行維護。 不過，有時不可能完全符合資源資料。 這是因為某些資訊可供參考裝置無法使用的硬體裝置使用。

幾乎所有的即時應用程式都會使用管線的 HAL 實作為。 當管線從硬體裝置切換至參照裝置時，轉譯作業會同時在硬體和軟體中完成。 當軟體裝置呈現時，會要求將資源下載至系統記憶體。 這可能需要在系統記憶體中快取的其他資源被收回，以騰出空間。

> [!Note]  
> 只有 Direct3D 10 和 Direct3D 10.1 才支援這個切換至參考層功能，而且在 Direct3D 11 和更新版本中已不再支援。

 

## <a name="thread-safe-layer"></a>Thread-Safe 層

這一層的設計目的是讓多執行緒應用程式從多個執行緒存取裝置。

Direct3D 10 應用程式可以使用裝置功能來控制裝置同步處理。 這可讓應用程式啟用/停用重要區段 (暫時啟用/停用多執行緒保護) ，以及在多個 Direct3D 10 API 進入點上取得/釋放重要區段鎖定。 預設會啟用執行緒安全層。 針對單一執行緒應用程式，執行緒安全層不會影響效能。



|                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 之間的差異：<br/> 與 Direct3D 9 不同的是，Direct3D 10 API 預設為完全安全線程。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的 API 功能 ](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




