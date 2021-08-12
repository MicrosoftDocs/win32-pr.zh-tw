---
title: 裝置參數
description: 裝置參數
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows媒體裝置管理員、裝置參數
- 裝置管理員，裝置參數
- 程式設計指南，裝置參數
- 服務提供者，裝置參數
- 建立服務提供者，裝置參數
- 裝置參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585347"
---
# <a name="device-parameters"></a>裝置參數

Windows媒體裝置管理員使用裝置參數來控制裝置的行為。 這些參數會依照裝置的安裝檔案中指定的方式新增至登錄， (INF 檔案) 。 下表列出 Windows 媒體裝置管理員查詢的裝置參數。



| 裝置參數名稱 | 登錄資料類型 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ SZ**        | 值，指定控制此裝置的服務提供者 CLSID。 此參數是 PnP 支援的必要參數。<br/> 參數值必須是 CLSID，而不是服務提供者的 ProgID。 此參數是在 Windows 媒體裝置管理員下支援隨插即用 (PnP) 的必要參數。 如需詳細資訊，請參閱 [為裝置啟用 PnP](enabling-pnp-for-devices.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | 選擇性值，指定在讀取和寫入作業期間 Windows 媒體裝置管理員使用的慣用傳輸大小。 如果未提供，則會使用預設的傳輸大小。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | 選擇性參數，指定 Windows 媒體裝置管理員在將裝置內容呈現給應用程式時，是否以中繼資料來組織內容。 若未指定，預設值是 0。<br/> 當應用程式列舉便攜音訊播放程式之存儲的內容時，Windows Media 裝置管理員可以呈現以中繼資料組織的內容。 這特別適用于具有大型儲存體容量的裝置。<br/> 應用程式和裝置能夠控制此行為。 裝置會透過裝置參數 *UseMetadataViews* 來指出其喜好設定。<br/> 以下是支援的兩個整數值：<br/> 要求在裝置的檔案系統上，將內容呈現給應用程式的方式完全相同。<br/> 要求將內容呈現給以中繼資料組織的應用程式。<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | 選擇性參數，指定裝置是否應該出現在 Windows 檔案總管中。 值1表示裝置應該會出現在 Windows 檔案總管中。 如需詳細資訊，請參閱[便攜音訊播放機的需求會出現在 Windows 檔案總管中](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | 選擇性參數，會警示 Windows 媒體裝置管理員服務提供者支援 **IMDSPDevice3**、 **IMDSPObject2** 和 **IMDSPStorage4**。 如果沒有這個旗標，Windows Media 裝置管理員將永遠不會呼叫這些介面。 值1表示支援這些介面。<br/> 與 Windows Media Player 同步處理的服務提供者需要此旗標。  (參閱[啟用與 Windows Media Player) 的同步處理](enabling-synchronization-with-windows-media-player.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**編碼 INF 檔案**

下列來自裝置 INF 檔案的範例程式碼示範如何在裝置安裝期間設定某些裝置參數。


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> <dt>

[**IMDServiceProvider2 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**IWMDMDevice 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





