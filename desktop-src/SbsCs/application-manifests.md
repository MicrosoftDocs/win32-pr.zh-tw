---
description: 所謂應用程式資訊清單，就是說明並識別共用和私用並存組件的 XML 檔，這些並存組件是應用程式要在執行時間加以繫結的組件。
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: 應用程式資訊清單
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106986423"
---
# <a name="application-manifests"></a>應用程式資訊清單

所謂應用程式資訊清單，就是說明並識別共用和私用並存組件的 XML 檔，這些並存組件是應用程式要在執行時間加以繫結的組件。 並存組件的版本必須與用來測試應用程式的組件版本相同。 應用程式資訊清單可能也會說明應用程式私用檔案的中繼資料。

如需 XML 架構的完整清單，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。

應用程式資訊清單具有下列元素和屬性。

| 項目                               | 屬性                | 必要 |
|---------------------------------------|---------------------------|----------|
| **裝配**                          |                           | Yes      |
|                                       | **manifestVersion**       | Yes      |
| **noInherit**                         |                           | No       |
| **assemblyIdentity**                  |                           | Yes      |
|                                       | **type**                  | Yes      |
|                                       | **name**                  | Yes      |
|                                       | **language**              | No       |
|                                       | **processorArchitecture** | No       |
|                                       | **version**               | Yes      |
|                                       | **publicKeyToken**        | No       |
| **相容性**                     |                           | No       |
| **應用程式**                       |                           | No       |
| **supportedOS**                       | **識別碼**                    | No       |
| **maxversiontested**                  | **識別碼**                    | No       |
| **依賴**                        |                           | No       |
| **y**                 |                           | No       |
| **file**                              |                           | No       |
|                                       | **name**                  | No       |
|                                       | **hashalg**               | No       |
|                                       | **hash**                  | No       |
| **activeCodePage**                    |                           | No       |
| **autoElevate**                       |                           | No       |
| **disableTheming**                    |                           | No       |
| **disableWindowFiltering**            |                           | No       |
| **DPIAware**                          |                           | No       |
| **DPIAwareness**                      |                           | No       |
| **gdiScaling**                        |                           | No       |
| **highResolutionScrollingAware**      |                           | No       |
| **longPathAware**                     |                           | No       |
| **printerDriverIsolation**            |                           | No       |
| **ultraHighResolutionScrollingAware** |                           | No       |
| **msix**                              |                           | No       |
| **heapType**                          |                           | No       |

## <a name="file-location"></a>檔案位置

應用程式資訊清單應該以資源的形式包含在應用程式的 EXE 檔案或 DLL 中。

如需詳細資訊，請參閱 [安裝並存元件](installing-side-by-side-assemblies.md)。

## <a name="file-name-syntax"></a>檔名語法

應用程式資訊清單檔的名稱是應用程式的可執行檔名稱，後面接著 .manifest。

例如，參考 example.exe 或 example.dll 的應用程式資訊清單會使用下列檔案名語法。 如果資源識別碼為1，您可以省略 <*資源識別碼*>] 欄位。

**example.exe。 <*資源識別碼*> 的資訊清單**

**example.dll。 <*資源識別碼*> 的資訊清單**

## <a name="elements"></a>元素

元素和屬性的名稱會區分大小寫。 元素和屬性的值不區分大小寫，但 type 屬性的值除外。

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a>組件

容器元素。 它的第一個子項目必須是 **noInherit** 或 **assemblyIdentity** 元素。 必要。

**Assembly** 元素必須在命名空間 "urn：架構-microsoft-com： asm" 中。 元件的子專案也必須在這個命名空間中，繼承或標記。

**Assembly** 元素具有下列屬性。



| 屬性           | 描述                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | **ManifestVersion** 屬性必須設定為1.0。 |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a>noInherit

在應用程式資訊清單中包含這個專案，以使用「無繼承」旗標來設定從資訊清單產生的 [啟用](activation-contexts.md) 內容。 當此旗標未在啟用內容中設定，且啟用內容為作用中時，會由相同進程、windows、視窗程式和 [非同步程序呼叫](/windows/desktop/Sync/asynchronous-procedure-calls)中的新執行緒繼承。 設定此旗標可防止新的物件繼承使用中的內容。

**NoInherit** 元素是選擇性的，通常會省略。 大部分的元件無法正確地使用「無繼承」啟用內容，因為元件必須明確設計來管理本身的啟用內容的傳播。 使用 **noInherit** 元素時，應用程式資訊清單所參考的任何相依元件都必須具有其 [組件資訊清單](assembly-manifests.md)中的 **noInherit** 元素。

如果在資訊清單中使用 **noInherit** ，它必須是 **元件** 專案的第一個子項目。 **AssemblyIdentity** 元素應該緊接在 **noInherit** 元素之後。 如果未使用 **noInherit** ， **assemblyIdentity** 必須是 **assembly** 專案的第一個子項目。 **NoInherit** 元素沒有任何子項目。 它不是 [組件資訊清單](assembly-manifests.md)中的有效元素。

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

作為 **元件** 專案的第一個子項目， **assemblyIdentity** 會描述和唯一識別擁有此應用程式資訊清單的應用程式。 **AssemblyIdentity** 是 **y** 專案的第一個子項目，描述應用程式所需的並存元件。 請注意，應用程式資訊清單中所參考的每個元件都需要 **assemblyIdentity** ，以完全符合參考元件本身的組件資訊清單中的 **assemblyIdentity** 。

**AssemblyIdentity** 元素具有下列屬性。 它沒有子項目。

| 屬性                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | 指定應用程式或元件類型。 值必須是 Win32，而且全部都是小寫。 必要。                                                                                                                                                                                                                                                                                                                              |
| **name**                  | 將應用程式或元件命名為唯一的名稱。 針對名稱，請使用下列格式： Organization.Division.Name。 例如，>mysampleapp。 必要。                                                                                                                                                                                                                                                               |
| **language**              | 識別應用程式或元件的語言。 選擇性。 如果應用程式或元件是特定語言，請指定 DHTML 語言代碼。 在適用于全球用途 (語言的應用程式 **assemblyIdentity** 中) 省略 language 屬性。<br/> 在適用于全球用途 (語言的元件 **assemblyIdentity** 中) 將 language 的值設定為 " \* "。<br/> |
| **processorArchitecture** | 指定處理器。 有效值包括 `x86`、`amd64`、`arm` 和 `arm64`。 選擇性。                                                                                                                                                                                                                                                                                                                       |
| **version**               | 指定應用程式或元件版本。 使用四部分版本格式：好吃. ooooo. ppppp。 以句號分隔的每個部分都可以是0-65535 （含）。 如需詳細資訊，請參閱 [元件版本](assembly-versions.md)。 必要。                                                                                                                                                                        |
| **publicKeyToken**        | 16字元的十六進位字串，表示用來簽署應用程式或元件之公開金鑰的 SHA-1 雜湊最後8個位元組。 用來簽署目錄的公開金鑰必須是2048位或更高的版本。 所有共用並存元件的必要項。                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a>相容性

包含至少一個 **應用程式**。 它沒有任何屬性。 選擇性。 沒有相容性元素的應用程式資訊清單預設為 windows 7 上的 Windows Vista 相容性。

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a>應用程式

包含至少一個 **supportedOS** 元素。 從 Windows 10 版本1903開始，它也可以包含一個選擇性的 **maxversiontested** 元素。 它沒有任何屬性。 選擇性。

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a>supportedOS

**SupportedOS** 元素具有下列屬性。 它沒有子項目。

| 屬性 | 說明   |
|-----------|-----------------------|
| **識別碼**    | 將識別碼屬性設定為 **{e2011457-1546-43c5-a5fe-008deee3d3f0}** ，以使用 Vista 功能來執行應用程式。 這可以讓針對 Windows Vista 設計的應用程式在較新的作業系統上執行。 <br/> 將識別碼屬性設定為 **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** ，以使用 Windows 7 功能來執行應用程式。<br/> 支援 Windows Vista、Windows 7 和 Windows 8 功能的應用程式不需要個別的資訊清單。 在此情況下，請新增所有 Windows 作業系統的 Guid。<br/> 如需 Windows 中 **識別碼** 屬性行為的詳細資訊，請參閱 [Windows 8 和 Windows Server 2012 相容性操作手冊](https://www.microsoft.com/download/details.aspx?id=27416)。<br/> 下列 Guid 對應于指出的作業系統：<br/> **{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10、windows server 2016 和 windows server 2019<br/> **{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 和 Windows Server 2012 R2<br/> **{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 和 Windows Server 2012<br/> **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> windows 7 和 windows Server 2008 R2<br/> **{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> windows Vista 和 windows Server 2008<br/> 您可以在 Windows 7 或 Windows 8. x 上進行測試，方法是執行資源監視器 (resmon) ，前往 [CPU] 索引標籤，以滑鼠右鍵按一下資料行標籤，選取 [選取資料行]，然後核取 [作業系統內容]。 在 Windows 8. x 上，您也可以在 [工作管理員 (taskmgr) 中找到此資料行。 資料行的內容會顯示找到的最大值或 "Windows Vista" 作為預設值。 <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a>maxversiontested

**Maxversiontested** 元素會指定測試應用程式所針對的 Windows 最大版本。 這是為了讓使用 [XAML 孤島](/windows/apps/desktop/modernize/xaml-islands) 且未部署在 MSIX 套件中的桌面應用程式使用。 在 Windows 10、1903版和更新版本中支援這個元素。

**Maxversiontested** 元素具有下列屬性。 它沒有子項目。

| 屬性 | 說明    |
|-----------|----------------|
| **識別碼**    | 將識別碼屬性設定為4部分版本字串，以指定測試應用程式所針對的 Windows 最大版本。 例如，"10.0.18226.0"。 |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>相依性

包含至少一個 **y**。 它沒有任何屬性。 選擇性。

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

**Y** 的第一個子項目必須是描述應用程式所需並存元件的 **assemblyIdentity** 元素。 每個 **y** 都必須正好在 **一個相依** 性內。 它沒有任何屬性。

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a>file

指定應用程式私用的檔案。 選擇性。

**File** 元素具有下表所示的屬性。



| 屬性   | 描述                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | 檔案的名稱。 例如，Comctl32.dll。                                                            |
| **hashalg** | 用來建立檔案雜湊的演算法。 此值應為 SHA1。                                 |
| **hash**    | 名稱所參考之檔案的雜湊。 長度的十六進位字串，取決於雜湊演算法。 |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a>activeCodePage

強制處理常式使用 UTF-8 作為程式字碼頁。

**activeCodePage** 已新增到 Windows 1903 版 (2019) 更新。 您可以宣告此屬性並在舊版 Windows 組建上執行，但是您必須如往常般處理舊版字碼頁偵測和轉換。 如需詳細資訊，請參閱 [使用 utf-8 字碼頁](/windows/uwp/design/globalizing/use-utf8-code-page) 。

這個元素沒有屬性。 **Utf-8** 只是 **activeCodePage** 元素的有效值。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a>autoElevate

指定是否啟用自動提升許可權。 **TRUE** 表示已啟用。 它沒有任何屬性。

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a>disableTheming

指定是否要為 UI 元素提供主題停用。 **TRUE** 表示已停用。 它沒有任何屬性。

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a>disableWindowFiltering

指定是否要停用視窗篩選。 **TRUE** 會停用視窗篩選，讓您可以從桌面列舉沉浸式視窗。 **disableWindowFiltering** 已加入 Windows 8 且沒有任何屬性。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a>DPIAware

指定目前的進程是否為每英寸的點 (DPI) 感知。

**Windows 10，版本1607：** 如果 **DPIAwareness** 元素存在，則會忽略 **DPIAware** 元素。 如果您想要為 Windows 10 的版本1607指定不同的行為，您可以在資訊清單中包含這兩個元素，而不是舊版作業系統。

下表描述根據 **DPIAware** 專案是否存在，以及它所包含的文字所產生的行為。 元素內的文字不區分大小寫。

| **DpiAware** 元素的狀態 | Description     |
|-----------------------------------|---------|
| Absent                            | 目前的進程預設為 DPI 感知。 您可以藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。                                                                                                                                                            |
| 包含 "true"                   | 目前的進程是系統 DPI 感知。                                                                                                                                                                                                                                                                                                                                                          |
| 包含 "false"                  | **Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。<br/> **Windows 8.1 和 Windows 10：** 目前的進程不感知 DPI，而且您無法藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，以程式設計方式變更此設定。<br/> |
| 包含 "true/pm"                | **Windows Vista、windows 7 和 Windows 8：** 目前的進程是系統 DPI 感知。<br/> **Windows 8.1 和 Windows 10：** 目前的進程是個別監視器 DPI 感知。<br/>                                                                                                                                                                                                          |
| 包含「每個監視器」            | **Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。<br/> **Windows 8.1 和 Windows 10：** 目前的進程是個別監視器 DPI 感知。<br/>                                                                                                                                                                                      |
| 包含任何其他字串         | **Windows Vista、windows 7 和 Windows 8：** 行為與 **DPIAware** 不存在時的行為相同。<br/> **Windows 8.1 和 Windows 10：** 目前的進程不感知 DPI，而且您無法藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，以程式設計方式變更此設定。<br/> |

如需 DPI 感知設定的詳細資訊，請參閱 [Dpi 感知層級的比較](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))。

**DPIAware** 沒有任何屬性。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a>DPIAwareness

指定目前的進程是否為每英寸的點 (DPI) 感知。

支援 **DPIAwareness** 元素之作業系統的最低版本是 Windows 10 1607 版。 針對支援 **DPIAwareness** 專案的版本， **DPIAwareness** 會覆寫 **DPIAware** 元素。 如果您想要為 Windows 10 的版本1607指定不同的行為，您可以在資訊清單中包含這兩個元素，而不是舊版作業系統。

**DpiAwareness** 元素可以包含單一專案或逗點分隔專案的清單。 在後者的情況下，會使用作業系統所辨識清單中第一個 (最左邊的) 專案。 如此一來，您就可以指定未來 Windows 作業系統版本所支援的不同行為。

下表描述根據 **DPIAwareness** 元素是否存在，以及其在最左邊辨識的專案中包含的文字所產生的行為。 元素內的文字不區分大小寫。

| **DPIAwareness** 元素狀態：        | Description                          |
|-----------------------------------------|-------------------------------------------|
| 元素不存在                       | **DpiAware** 元素會指定進程是否為 DPI 感知。                                                                                                                                                                   |
| 未包含任何可識別的專案            | 目前的進程預設為 DPI 感知。 您可以藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。 |
| 第一個被辨識的專案是 "system"       | 目前的進程是系統 DPI 感知。                                                                                                                                                                                               |
| 第一個被辨識的專案是 "permonitor"   | 目前的進程是個別監視器 DPI 感知。                                                                                                                                                                                          |
| 第一個被辨識的專案是 "permonitorv2" | 目前的進程會使用每個監視器-v2 DPI 感知內容。 此專案只會在 Windows 10 版本1703或更新版本上識別。                                                                                              |
| 第一個被辨識的專案是「不知道」      | 目前的進程不會察覺 DPI。 您 **無法** 藉由呼叫 [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) 或 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數，以程式設計方式變更此設定。      |

如需此元素所支援之 DPI 感知設定的詳細資訊，請參閱 [DPI \_ 感知](/windows/desktop/api/windef/ne-windef-dpi_awareness) 和 [DPI \_ 感知 \_ 內容](/windows/desktop/hidpi/dpi-awareness-context)。

**DPIAwareness** 沒有任何屬性。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a>gdiScaling

指定是否啟用 GDI 縮放比例。 支援 **gdiScaling** 元素之作業系統的最低版本是 Windows 10 版本1703。

GDI (圖形裝置介面) framework 可以針對個別監視器將 DPI 縮放比例套用至基本和文字，而不需要更新應用程式本身。 這對於不會再主動更新的 GDI 應用程式很有用。

非向量圖形 (例如點陣圖、圖示或工具列) 無法由此元素縮放。 此外，在應用程式動態建立的點陣圖內出現的圖形和文字也無法由此元素進行縮放。

**TRUE** 表示已啟用這個元素。 它沒有任何屬性。


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a>highResolutionScrollingAware

指定是否啟用高解析度滾動感知功能。 **TRUE** 表示已啟用。 它沒有任何屬性。

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a>longPathAware

啟用長度超過 **MAX_PATH** 的長路徑。 在 Windows 10、1607版和更新版本中支援這個元素。 如需詳細資訊，請參閱[這篇文章](../fileio/maximum-file-path-limitation.md)。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a>printerDriverIsolation

指定是否啟用印表機驅動程式隔離。 **TRUE** 表示已啟用。 它沒有任何屬性。 印表機驅動程式隔離可讓印表機驅動程式在與執行列印多工緩衝處理器不同的處理常式中執行，藉以改善 Windows 列印服務的可靠性。 在 Windows 7 和 Windows Server 2008 R2 中開始支援印表機驅動程式隔離。 應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以獨立于印表機驅動程式，並改善其可靠性。 也就是說，如果印表機驅動程式發生錯誤，應用程式將不會損毀。


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a>ultraHighResolutionScrollingAware

指定是否啟用超高解析度-滾動功能感知功能。 **TRUE** 表示已啟用。 它沒有任何屬性。

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a>msix

為目前的應用程式指定 [稀疏 MSIX 封裝](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) 的身分識別資訊。 在 Windows 10、2004版和更新版本中支援這個元素。

**Msix** 元素必須在命名空間中 `urn:schemas-microsoft-com:msix.v1` 。 它包含下表所示的屬性。

| 屬性   | 描述                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **publisher**    | 描述發行者資訊。 這個值必須符合您的稀疏套件資訊清單中 [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity)元素的 **發行者** 屬性。 |
| **packageName** | 描述封裝的內容。 這個值必須符合您的稀疏套件資訊清單中 [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity)元素的 **Name** 屬性。    |
| **applicationId**    | 應用程式的唯一識別碼。 這個值必須符合您的稀疏套件資訊清單中 [應用程式](/uwp/schemas/appxpackage/uapmanifestschema/element-application)元素的 **識別碼** 屬性。  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a>heapType

覆寫 [Win32 堆積 api](../Memory/heap-functions.md) 要使用的預設堆積執行。

* 值 **SegmentHeap** 表示將使用區段堆積。 區段堆積是新式的堆積執行，通常會降低整體記憶體的使用量。 Windows 10 2004 版 (build 19041) 和更新版本支援這個元素。
* 所有其他值都會被忽略。

這個元素沒有屬性。

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a>範例

以下是名為 MySampleApp.exe 之應用程式的應用程式資訊清單範例。 應用程式會使用 SampleAssembly 並存元件。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
