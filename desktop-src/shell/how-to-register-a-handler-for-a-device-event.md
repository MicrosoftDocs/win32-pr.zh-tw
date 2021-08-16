---
description: 描述在登錄中執行裝置事件處理常式的進程。
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: 如何註冊裝置事件的處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859597"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>如何註冊裝置事件的處理常式

處理常式會定義自動播放的軟體部分。 它們定義軟體的圖示和易記名稱，以及元件物件模型 (COM) 元件具現化，以及如何初始化元件以回應事件。 特定事件的每個處理常式都會註冊為適當 **EventHandler** 索引鍵下的值。 當偵測到該事件時，系統會提示使用者從所有針對該事件註冊的處理常式清單中選擇處理常式。

## <a name="instructions"></a>指示


處理常式及其相關聯的值會定義在 **AutoplayHandlers** \\ **處理常式** 索引鍵下。 子機碼會因系統是否可以直接讀取裝置內容，或裝置是否透過專屬介面提供內容給系統而有所不同。

下列範例顯示裝置所使用的子機碼和值，例如數位攝影機或 .mp3 播放機，可透過專屬介面提供其內容給系統。 範例處理常式稱為 **MyHandler**。

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> 雖然此範例顯示 ProgID 和類別識別碼 (CLSID) 值，但實際上這些值是互斥的，因此只會有一個或另一個。 首選 ProgID 值。 無論使用哪種方式，都應該指向實 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面的 COM 元件。

 

您可以輸入動作值做為常值（例如，如本範例所示的「播放音樂」），或輸入包含資源字串的檔案名。 您也可以輸入提供者值做為常值，或輸入包含資源字串的檔案名。 自動播放會將動作值和提供者值與 "using" 這個字結合，以建立在 UI 中顯示的易記標題。 在此範例中，產生的標題是「使用 Windows Media Player 播放音樂」。

DefaultIcon 值指向 .ico 檔案或二進位檔案中的資源。 如果二進位檔案名之後的數值是零或大於零，則它是該二進位檔案中圖示的索引值。 如果是負值，則它是圖示資源識別碼。 建議使用負的索引值。 .Ico 檔案的案例中不需要任何值。 建議您在路徑中使用環境變數。

InitCmdLine 值會在呼叫任何其他方法之前，透過 [**IHWEventHandler：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) 方法原封不動地傳遞。

下列範例顯示可直接讀取的裝置（例如 CD-ROM 光碟機或其他卸載式磁片）所使用的子機碼和值。 同樣地，範例處理常式稱為 **MyHandler**。

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

在此範例中，動作和提供者值會顯示為包含資源字串的檔案名，而不是常值，但它們參考的字串會以相同的方式使用。 它們會與 "using" 這個字結合，以形成易記的標題，如稍早所述。

InvokeProgID 和 InvokeVerb 值會取代 CLSID、InitCmdLine 和 ProgID。 InvokeProgID 和 InvokeVerb 值符合在 **HKEY \_ 類別 \_ 根目錄** 下找到的索引鍵名稱，如下列登錄專案所示。 這組範例索引鍵會對應至稍早所述的特定處理常式範例。

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函數會使用 CLSID 來執行適當的應用程式。

在您以這兩種方式之一定義處理常式之後，您需要針對特定事件註冊處理常式。 若要這麼做，請將處理常式名稱提供為 **EventHandlers** 下該事件索引鍵的值。 下列範例顯示如何將 **MyHandler** 註冊為 GenericVolumeArrival 事件的處理常式。 它沒有指派的資料值。

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
