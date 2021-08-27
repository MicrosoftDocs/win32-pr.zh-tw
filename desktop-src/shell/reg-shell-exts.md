---
description: 您必須先註冊 Shell 擴充處理常式物件，Shell 才能使用它。 本主題是如何註冊 Shell 擴充處理常式的一般討論。
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: 註冊 Shell 延伸模組處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111208"
---
# <a name="registering-shell-extension-handlers"></a>註冊 Shell 延伸模組處理常式

您必須先註冊 Shell 擴充處理常式物件，Shell 才能使用它。 本主題是如何註冊 Shell 擴充處理常式的一般討論。

每當您建立或變更 Shell 延伸模組處理常式時，請務必通知系統您已進行變更。 若要這麼做，請呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)，並指定 **SHCNE \_ ASSOCCHANGED** 事件。 如果您未呼叫 **SHChangeNotify**，在系統重新開機之前，可能無法辨識變更。

有一些其他因素適用于 Windows 2000 系統。 如需詳細資訊，請參閱[Windows 2000 系統上的註冊 Shell 擴充處理常式](#registering-shell-extension-handlers)一節。

如同所有元件物件模型 (COM) 物件，您必須使用 Windows 軟體開發套件 (SDK) 提供的工具（例如 Guidgen.exe）來建立處理常式的 GUID。 在 **HKEY \_ 類別 \_ 根目錄** CLSID 下建立子機碼， \\ 其名稱是該 GUID 的字串形式。 由於 Shell 擴充處理常式是同進程伺服器，因此您也必須在該 GUID 子機碼底下建立 **InprocServer32** 子機碼，並將 (預設) 值設定為處理常式 DLL 的路徑。 使用單元執行緒模型。 以下顯示一個範例：

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

每當 Shell 採取的動作都可能牽涉到 Shell 擴充處理常式時，就會檢查適當的登錄子機碼。 擴充功能處理常式在呼叫時，所使用的子機碼控制項。 比方說，當 Shell 針對 [檔案類型](fa-file-types.md)的成員顯示快捷方式功能表時，會呼叫快捷方式功能表處理常式，是常見的作法。 在此情況下，處理常式必須在檔案類型的 **ProgID** 子機碼下註冊。

本主題將討論下列主題：

-   [處理常式名稱](#handler-names)
-   [預先定義的 Shell 物件](#predefined-shell-objects)
-   [擴充處理常式註冊的範例](#example-of-an-extension-handler-registration)
    -   [註冊 Shell 延伸模組處理常式](#registering-shell-extension-handlers)
-   [相關主題](#related-topics)

## <a name="handler-names"></a>處理常式名稱

若要啟用 Shell 延伸模組處理常式，請使用處理程式子機碼名稱來建立子機碼 (在 [檔) 類型] 的 **ProgID** (的 [ **ShellEx** ] 子機碼下) ，或 ([預先定義之 \_ shell \_ 物件](handlers.md)的 [shell 物件類型名稱) ]。

例如，如果您想要註冊 Myprogram.exe 的快捷方式功能表延伸模組處理常式，請先建立下列子機碼：

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

針對下列處理常式，請在名為的「處理常式子機碼名稱」子機碼底下建立子機碼，並將其命名為 Shell 延伸模組 (CLSID) 的字串版本。 藉由建立多個子機碼，可以在處理常式子機碼名稱下註冊多個擴充功能。



| 處理常式                 | 介面          | 處理常式子機碼名稱       |
|-------------------------|--------------------|---------------------------|
| 資料行提供者處理常式 | IColumnProvider    | **ColumnHandlers**        |
| 快速鍵功能表處理常式   | ICoNtextMenu       | **CoNtextMenuHandlers**   |
| Copyhook 處理常式        | ICopyHook          | **CopyHookHandlers**      |
| 拖放功能處理常式   | ICoNtextMenu       | **DragDropHandlers**      |
| 屬性工作表處理常式  | IShellPropSheetExt | **PropertySheetHandlers** |



 

針對下列處理常式，「處理常式子機碼名稱」索引鍵的預設值是 Shell 延伸模組之 CLSID 的字串版本。 您只能為這些處理常式註冊一個擴充功能。



| 處理常式                 | 介面            | 處理常式子機碼名稱                        |
|-------------------------|----------------------|--------------------------------------------|
| 資料處理程式            | IDataObject          | **DataHandler**                            |
| 捨棄處理常式            | IDropTarget          | **DropHandler**                            |
| 圖示處理常式            | IExtractIconA/W      | **IconHandler**                            |
| 縮圖影像處理常式 | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| 資訊提示處理常式         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
|  (ANSI) 的 Shell 連結       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Shell 連結 (UNICODE)     | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| 結構化儲存體      | IStorage             | **{0000000B-0000-0000-C000-000000000046}** |
| 中繼資料                | IPropertySetStorage  | **PropertyHandler**                        |
| 釘選到開始功能表       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| 釘選到工作列          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

只有包含 [IsShortCut](./links.md)專案的檔案類型才需要指定的子機碼，以將 [釘選到 **開始] 功能表** 和 [**釘選到工作列**] 新增至專案的快捷方式功能表。

## <a name="predefined-shell-objects"></a>預先定義的 Shell 物件

Shell 會在 **HKEY \_ 類別 \_ 根目錄** 下定義其他物件，其可透過與檔案類型相同的方式來擴充。 例如，若要新增所有檔案的屬性工作表處理常式，您可以在 **PropertySheetHandlers** 子機碼下註冊。

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

下表提供 **HKEY \_ 類別 \_ 根目錄** 的各種子機碼，您可以在這些子機碼下註冊擴充處理常式。 請注意，許多擴充程式處理常式無法在所有列出的子機碼下註冊。 如需進一步的詳細資料，請參閱特定處理常式的檔。



| 子機碼                    | 描述                                                          | 可能的處理常式                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | 所有檔案                                                            | 快速鍵功能表、屬性工作表、動詞 (請參閱以下)  |
| **AllFileSystemObjects**  | 所有檔案和檔案資料夾                                           | 快速鍵功能表、屬性工作表、動詞             |
| **資料夾**                | 全部資料夾                                                          | 快速鍵功能表、屬性工作表、動詞             |
| **目錄**             | 資料夾                                                         | 快速鍵功能表、屬性工作表、動詞             |
| **目錄 \\ 背景** | 檔案資料夾背景                                               | 僅快捷方式功能表                               |
| **DesktopBackground**     | 桌面背景 (Windows 7 和更新版本)                             | 快捷方式功能表，動詞                             |
| **磁碟機**                 | MyComputer 中的所有磁片磁碟機，例如 "C： \\ "                             | 快速鍵功能表、屬性工作表、動詞             |
| **Network**               | 網路下的整個網路 ()                              | 快速鍵功能表、屬性工作表、動詞             |
| **網路 \\ 類型\\\#**     |  (類型的所有物件 \# 如下所示)                                    | 快速鍵功能表、屬性工作表、動詞             |
| **NetShare**              | 所有網路共用                                                   | 快速鍵功能表、屬性工作表、動詞             |
| **NetServer**             | 所有網路伺服器                                                  | 快速鍵功能表、屬性工作表、動詞             |
| *網路 \_ 提供者 \_ 名稱* | 網路提供者「*網路 \_ 提供者 \_ 名稱*」提供的所有物件 | 快速鍵功能表、屬性工作表、動詞             |
| **印表機**              | 所有印表機                                                         | 快速鍵功能表，屬性工作表                    |
| **AudioCD**               | CD 光碟機中的音訊 CD                                                 | 僅限動詞                                       |
| **DVD**                   | DVD 光碟機 (Windows 2000)                                              | 快速鍵功能表、屬性工作表、動詞             |



 

### <a name="notes"></a>備註

-   您可以用滑鼠右鍵按一下檔案資料夾，而不是在資料夾的任何內容中，來存取檔案資料夾背景快捷方式功能表。
-   「動詞」是在 **HKEY \_ 類別 \_ 根** 子機碼 \\  \\ **Shell** \\ **動詞** 命令下註冊的特殊命令。
-   針對 **網路** \\ **類型** \\ **\#** ，" \# " 是十進位中的網路提供者類型代碼。 網路提供者類型代碼是網路類型的最高文字。 網路類型清單是在 Winnetwk 中提供的， (WNNC \_ NET \_ \* values) 。 例如，WNNC \_ NET \_ SHIVA 是0x00330000，因此對應的型別子機碼會是 **HKEY 類別的 \_ \_ ROOT** \\ **Network** \\ **type** \\ **51**。
-   「*網路 \_ 提供者 \_ 名稱*」是 [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)所指定的網路提供者名稱，並已將空格轉換成底線。 例如，如果已安裝 Microsoft 網路網路提供者，其提供者名稱為 "microsoft Windows network"，而對應的 *網路 \_ 提供者 \_ 名稱* 為 **Microsoft \_ Windows \_ network**。

## <a name="example-of-an-extension-handler-registration"></a>擴充處理常式註冊的範例

若要啟用特定處理常式，請使用處理程式的名稱，在擴充處理常式類型子機碼底下建立子機碼。 Shell 不會使用處理程式的名稱，但它必須與該類型子機碼下的所有其他名稱不同。 將名稱子機碼的預設值設定為處理常式 GUID 的字串形式。

下列範例說明使用 myp 檔案類型啟用快捷方式功能表和屬性工作表延伸模組處理常式的登錄專案。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>註冊 Shell 延伸模組處理常式

本章節中討論的註冊程式必須遵循所有 Windows 系統。 不過，在稍後的系統中，可能需要額外的步驟。 因為這些較新版本的 Windows 是設計用來在受控環境中使用，所以對登錄的存取權可能會受到系統管理限制，而不需要像上一節所述安裝稍微不同的方法。

> [!Note]  
> 安裝程式通常不應該直接寫入登錄中。 相反地，您應該使用 Windows Installer 套件來完成安裝程式。 這些工具可確保軟體正常執行，並提供對每個使用者類別註冊等功能的存取。

 

Shell 擴充處理常式會在 Shell 進程中執行。 由於它是系統進程，因此系統管理員可以藉由將 **Explorer** 索引鍵的 EnforceShellExtensionSecurity 值設定為1，將 Shell 擴充處理常式限制在已核准清單上的處理常式，如下所示：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

若要將 Shell 擴充處理常式放在核准的清單上，請建立 **REG \_ SZ** 值，其名稱是在 **已核准** 子機碼下的處理常式 GUID 字串形式。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

例如，下列範例會將 *MyCommand* 和 *MyPropSheet* 處理常式新增至核准的清單。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

Shell 不會使用指派給 GUID 的值，但應該設定為讓檢查登錄變得更容易。

如果安裝應用程式的人員具有足夠的許可權，則您的安裝程式應用程式可以將值新增至 **核准** 的子機碼。 如果嘗試新增延伸模組處理常式失敗，您應該通知使用者需要系統管理許可權才能完整安裝應用程式。 如果處理常式對應用程式而言是必要的，您應該會使設定失敗，並通知使用者與系統管理員聯絡。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[初始化 Shell 擴充處理常式](int-shell-exts.md)
</dt> </dl>

 

 
