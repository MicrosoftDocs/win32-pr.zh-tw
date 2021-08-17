---
title: 軟體層
description: Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。 本節說明每個圖層的功能。
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59d0405d53526b8fb0b93e52fd1a53b5c17839f6c58df919bac335b21ad2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124359"
---
# <a name="software-layers"></a>軟體層

Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。 本節說明每個圖層的功能。

一般來說，圖層會加入功能，但不會修改現有的行為。 例如，除了要具現化的調試層之外，核心函式的傳回值也會與所具現化的調試層有相同的傳回值。

若要在建立裝置時建立圖層，請呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ，並提供一或多個 [**D3D11 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) 標值。

Direct3D 11 提供下列執行時間層級：

-   [核心層](#core-layer)
-   [Debug 圖層](#debug-layer)
-   [相關主題](#related-topics)

## <a name="core-layer"></a>核心層

核心層預設為存在;在 API 和設備磁碟機之間提供非常精簡的對應，將高頻率呼叫的額外負荷降至最低。 因為核心層是效能不可或缺的，所以它只會執行重大驗證。 其餘層是選擇性的。

## <a name="debug-layer"></a>Debug 圖層

Debug 層提供大量的額外參數和一致性驗證 (例如驗證著色器連結和資源系結、驗證參數一致性，以及報告錯誤描述) 。

若要建立支援 debug 層的裝置，您必須安裝 (的 DirectX SDK，才能取得 D3D11SDKLayers.dll) ，然後在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函式或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)函式時，指定 **D3D11 \_ 建立 \_ 裝置的 \_ 調試** 程式旗標。 如果您在啟用調試層的情況下執行應用程式，應用程式將會大幅降低。 但是，為了確保您的應用程式在出貨之前已清除錯誤和警告，請使用 debug 層。 如需詳細資訊，請參閱 [使用 debug layer 來偵測應用程式](using-the-debug-layer-to-test-apps.md)。


> [!Note]  
> 若為 Windows 7 （Windows 7 (KB2670838) 或 Windows 8）的平臺更新，若要建立支援 debug 層的裝置，請安裝 Windows 軟體開發套件 (SDK) ，以取得 D3D11 \_ Windows 8。


> [!Note]  
> 針對 Windows 10，若要建立支援 debug 層的裝置，請啟用 [圖形工具] 選用功能。 移至 [系統]、[應用程式] & [功能]、[管理選擇性功能]、[新增功能]，然後尋找 [圖形工具] 下的設定面板。


> [!Note]  
> 如需有關如何從遠端偵測 DirectX 應用程式的詳細資訊，請參閱 [從遠端偵錯 directx 應用程式](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)。

 

或者，您也可以使用 directx SDK 隨附的 [directx 主控台](/previous-versions//bb219725(v=vs.85)) 來啟用/停用偵錯工具旗標。

當 debug 圖層列出記憶體流失時，它會輸出物件介面指標清單及其易記名稱。 預設的易記名稱是「 &lt; 未命名」 &gt; 。 您可以使用 [**ID3D11DeviceChild：： SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) 方法以及 D3Dcommon 中的 **WKPDID \_ D3DDebugObjectName** GUID 來設定易記名稱。 例如，若要以 SDKLayer 名稱 mytexture.jpg 命名 pTexture，請使用下列程式碼：


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



一般而言，您應該從生產版本編譯這些呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 