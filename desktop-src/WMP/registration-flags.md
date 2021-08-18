---
title: 註冊旗標
description: 註冊旗標
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player 外掛程式、註冊旗標
- 外掛程式，註冊旗標
- 使用者介面外掛程式、註冊旗標
- UI 外掛程式、註冊旗標
- 旗標，使用者介面外掛程式
- 登錄，UI 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002808"
---
# <a name="registration-flags"></a>註冊旗標

當 Windows Media Player 外掛程式 Wizard 建立新的 UI 外掛程式專案時，它會在登錄中建立一個機碼，其中包含外掛程式的相關資訊。 此金鑰會建立在下列位置：


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassId* 是外掛程式的類別識別碼。

此索引鍵包含下列值。



| 名稱                     | 類型       | 描述                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 功能             | REG \_ DWORD | DWORD 值，其中至少包含一個外掛程式類型旗標，該旗標可以使用二進位或作業結合一或多個外掛程式功能旗標。                             |
| 描述              | REG \_ SZ    | 字串，其中包含外掛程式的描述。 外掛程式 wizard 會建立字串資源，並使用此值的 res 通訊協定) 來提供資源 (的 URL。         |
| FriendlyName             | REG \_ SZ    | 字串，包含外掛程式的使用者可讀取名稱。 外掛程式 wizard 會建立字串資源，並使用此值的 res 通訊協定) 來提供資源 (的 URL。 |
| UninstallPath (選用)  | REG \_ SZ    | 字串，包含卸載外掛程式之可執行檔的路徑。                                                                                                        |



 

如需 res 通訊協定的詳細資訊，請參閱網際網路開發 SDK。

下表詳細說明外掛程式類型旗標。



| 外掛程式類型旗標                | 值 | 描述                                       |
|----------------------------------|-------|---------------------------------------------------|
| **外掛程式 \_ 類型 \_ 背景**     | 0x1   | UI 外掛程式不會顯示使用者介面。 |
| **外掛程式 \_ 類型 \_ SEPARATEWINDOW** | 0x2   | UI 外掛程式是個別的視窗外掛程式。      |
| **外掛程式 \_ 類型 \_ DISPLAYAREA**    | 0x3   | UI 外掛程式是顯示區域外掛程式。         |
| **外掛程式 \_ 類型 \_ SETTINGSAREA**   | 0x4   | UI 外掛程式是設定區域外掛程式。        |
| **外掛程式 \_ 類型 \_ METADATAAREA**   | 0x5   | UI 外掛程式是中繼資料區域外掛程式。        |



 

下表詳細說明外掛程式功能旗標。



| 外掛程式功能旗標             | 值      | 描述                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **外掛程式 \_ 旗標 \_ ACCEPTSMEDIA**       | 0x10000000 | 當 Windows Media Player 呼叫 [**IWMPPluginUI：： SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)時，UI 外掛程式可以接受 **媒體** 物件指標陣列。                                                                                                                                                                                                                                                           |
| **外掛程式 \_ 旗標 \_ ACCEPTSPLAYLISTS**   | 0x8000000  | 當 Windows Media Player 呼叫 [**IWMPPluginUI：： SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)時，UI 外掛程式可以接受 **播放清單** 物件指標陣列。                                                                                                                                                                                                                                                        |
| **外掛程式 \_ 旗標 \_ HASPRESETS**         | 0x4000000  | UI 外掛程式會使用預設值。 如果外掛程式指定此旗標，Windows Media Player 會呼叫 [**IWMPPluginUI：： GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) ，以查詢外掛程式是否有預設的資訊。                                                                                                                                                                                                      |
| **外掛程式 \_ 旗標 \_ HASPROPERTYPAGE**    | 0x80000000 | UI 外掛程式提供屬性頁對話方塊。 如果叫用屬性頁時設定這個旗標，Windows Media Player 會呼叫 [**IWMPPluginUI：:D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) 。                                                                                                                                                                                                 |
| **外掛程式 \_ 旗標 \_ 隱藏**             | 0x02000000 | 背景 UI 外掛程式不會出現在從 [ **View** ] 或 [ **Tools** ] 功能表中存取的 [**外掛程式]** 功能表上，或現在現正播放的 [**立即播放] 選項** 按鈕。 它會出現在 [選項] 對話方塊的 [ **外掛程式** ] 索引標籤上。 這會導致背景外掛程式執行圖示出現在狀態列中。此旗標不會影響背景 UI 外掛程式以外的外掛程式。<br/> |
| **外掛程式 \_ 旗標 \_ INSTALLAUTORUN**     | 0x40000000 | 當安裝外掛程式時，Windows Media Player 會自動執行 UI 外掛程式。                                                                                                                                                                                                                                                                                                                               |
| **外掛程式 \_ 旗標 \_ LAUNCHPROPERTYPAGE** | 0x20000000 | 當 UI 外掛程式第一次執行時，Windows Media Player 會呼叫 [**IWMPPluginUI：:D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) 。如果指定此旗標，則也應該指定 **外掛程式 \_ 旗標 \_ HASPROPERTYPAGE** 。<br/>                                                                                                                                                             |



 

下列常數定義于 wmpplug 中。 請勿變更與這些常數相關聯的值。



| 名稱                                    | 描述                               |
|-----------------------------------------|-------------------------------------------|
| **外掛程式 \_ INSTALLREGKEY**               | 外掛程式登錄機碼的位置。 |
| **外掛程式 \_ INSTALLREGKEY \_ FRIENDLYNAME** | 易記名稱值的名稱。      |
| **外掛程式 \_ INSTALLREGKEY \_ 描述**  | 描述值的名稱。        |
| **外掛程式 \_ INSTALLREGKEY \_ 功能** | 功能值的名稱。       |
| **外掛程式 \_ INSTALLREGKEY \_ 卸載**    | 卸載路徑值的名稱。     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPPluginUI：:D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI：： GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI：： SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**消費者介面外掛程式程式設計參考**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





