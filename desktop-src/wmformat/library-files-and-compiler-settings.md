---
title: 程式庫檔案和編譯器設定
description: 程式庫檔案和編譯器設定
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows媒體格式 SDK，程式庫檔案
- Windows媒體格式 SDK，編譯器設定
- Windows媒體格式 SDK，標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176f6c7acb9516e8c7ac38a067091bcbb0c8f7cf49cfdb9e65b396768158b233
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930658"
---
# <a name="library-files-and-compiler-settings"></a>程式庫檔案和編譯器設定

若要使用 Windows 媒體格式 SDK 來開發應用程式，您必須使用 Microsoft Visual C++ 6.0 版或更新版本。 唯一適用于開發的程式設計語言是 c + + 和 C。

下表說明此 SDK 隨附之各種標頭檔的內容。



| 標頭檔                 | 描述                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr。h                    | 定義與 ASF 檔案作業相關的錯誤碼。 此標頭包含在 wmsdk 中。                                                                                                                                                            |
| drmexternals。h              | 定義用於數位版權管理 (DRM) 的結構、列舉和常數。 撰寫使用 DRM 的應用程式時，請包含此標頭。                                                                                            |
| dshowasf。h                  | 定義 Microsoft DirectShow QASF 篩選準則。 撰寫可建立或讀取 ASF 檔案的 DirectShow 應用程式時，請包含此標頭。 如需詳細資訊，請參閱[DirectShow 和 Windows 媒體](directshow-and-windows-media.md)。               |
| msnetobj。h                  | 定義 [**IRMGetLicense**](irmgetlicense.md)介面，此介面是在隨 Windows 媒體格式 SDK 安裝的其中一個執行時間程式庫中所執行。                                                                                     |
| nserror。h                   | 定義 Windows 媒體技術的錯誤碼。 只有這些錯誤碼的子集與 Windows 媒體格式 SDK 有關。 此標頭包含在 wmsdk 中。                                                                            |
| wmdxva。h                    | 包含啟用 Microsoft DirectX Video 加速播放 Windows 媒體型內容時所需的其他標頭和定義。 如需詳細資訊，請參閱 [啟用 DirectX Video 加速](enabling-directx-video-acceleration.md)。 |
| wmnetsourcecreator。h        | 包含建立網路來源外掛程式所需的資訊。                                                                                                                                                                                      |
| wmsbuffer。h                 | 定義緩衝區物件所使用的介面。 建立您自己的緩衝區以讀取檔案時，請包含此標頭。                                                                                                                                 |
| wmsdk。h                     | 使用 Windows 媒體格式 SDK 之應用程式的主要標頭。 此標頭不包含任何定義，但包含 asferr .h、nserror .h、windows .h 和 wmsdkidl .h。 使用此 SDK 的所有應用程式都包含此標頭。                     |
| wmsdkidl。h                  | 針對 Windows 媒體格式 SDK 的大部分物件定義介面、函數、結構、列舉和常數。 此標頭包含在 wmsdk 中。                                                                             |
| wmsinternaladminnetsource。h | 定義網路來源外掛程式的介面。                                                                                                                                                                                                  |
| wmsysprf。h                  | 定義系統設定檔的常數。 在依識別碼載入系統設定檔的應用程式中包含此標頭。                                                                                                                         |



 

若要使用 Windows 媒體格式 SDK，必須正確設定您的編譯器。 設定在偵錯工具模式中的建立方式不同于發行模式。 根據下表設定您的設定。 所有這些設定都是在 Project 設定] 對話方塊中設定。 若要進入對話方塊，請從 [ **Project** ] 功能表中選取 [**設定**]。



| 設定                                                                 | Debug 值                                                                              | 版本值                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
|  (C/c + +] 索引標籤、類別 = 程式碼產生) 使用執行時間程式庫            | Debug 多執行緒 DLL                                                                  | 多執行緒 DLL                                                                       |
|  (連結] 索引標籤的 [分類 = 一般) 忽略所有預設程式庫] (核取方塊)  | 已選取                                                                                 | 已選取                                                                                |
|  (連結索引標籤、分類 = 一般) 物件/程式庫模組                   | 包含 Msvcrtd.lib .lib 和 Wmvcore.lib.Do 不包含 Libc .lib 或任何變異。<br/> | 包含 Msvcrt.lib .lib 和 Wmvcore.lib.Do 不包含 Libc .lib 或任何變異。<br/> |



 

如果您使用 Microsoft Visual Studio .net，則設定已變更為不同的位置，如下表所示。 所有這些設定都是在 [ **屬性頁** ] 對話方塊中設定。 若要進入對話方塊，請在 [ **方案總管** ] 窗格中，以滑鼠右鍵按一下您的專案，然後從內容功能表中選取 [ **屬性** ]。



| 設定                                                                  | Debug 值                                                                              | 版本值                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
|  (設定屬性/C/c + +/程式碼產生) 執行時間程式庫     | 多執行緒調試 DLL (/MDd)                                                           | 多執行緒 DLL (/MD)                                                                 |
|  (設定屬性/連結器/輸入) 其他相依性      | 包含 Msvcrtd.lib .lib 和 Wmvcore.lib.Do 不包含 Libc .lib 或任何變異。<br/> | 包含 Msvcrt.lib .lib 和 Wmvcore.lib.Do 不包含 Libc .lib 或任何變異。<br/> |
|  (設定屬性/連結器/輸入) 略過所有預設程式庫 | 是                                                                                      | 是                                                                                     |



 

如果您想要延遲載入 Wmvcore.dll 或任何其他 DLL，請使用 Microsoft Visual C++ 6.0 中的連結選項/DELAYLOAD，或在 Microsoft Visual C++ .net 中延遲載入的 dll。

此外，您還需要包含 Windows 媒體格式 SDK 的程式庫和標頭的目錄。 若要尋找 Visual C++ 6.0 的目錄設定，請按一下 [**工具**] 功能表上的 [**選項**]，然後按一下 [**目錄**] 索引標籤。使用 Visual C++ .net 時，請按一下 [**工具**] 功能表上的 [**選項**]，然後選取 [選項] 清單中的 [專案]/[VC++ 目錄]。 如下表所示，新增目錄。 如果您變更了 Windows 媒體格式 SDK 的安裝目錄，您的路徑將會不同。



| 目錄類型 | 預設路徑                 |
|----------------|------------------------------|
| Include 檔案  | C： \\ WMSDK \\ WMFSDK11 \\ include |
| 程式庫檔案  | C： \\ WMSDK \\ WMFSDK11 \\ lib     |



 

如果您使用 Platform SDK，則預設路徑會如下所示：



| 目錄類型 | 預設路徑                                              |
|----------------|-----------------------------------------------------------|
| Include 檔案  | C： \\ Program Files \\ Microsoft SDsK \\ Windows \\ 6.0 版 \\ 包含 |
| 程式庫檔案  | C： \\ Program Files \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ Lib     |



 

在呼叫任何建立函式之前，COM 應該使用 **Coinitialize** 或 **CoinitializeEx** 的呼叫來初始化。 您可以使用自由執行緒模型或單元執行緒模型，但單元執行緒模型會在應用程式上強加執行緒限制。 如需 Microsoft 元件物件模型 (COM) 的詳細資訊，請參閱 [Microsoft 網站](../com/the-component-object-model.md)上的 com 頁面。

**注意** 播放或建立受數位 Rights Management (DRM) 保護之檔案的應用程式，需要個別的靜態程式庫，必須與 Microsoft 分開取得。 如需詳細資訊，請參閱[Microsoft](https://www.microsoft.com/licensing/default)網站上的 Windows 媒體授權表單。 如果您使用 DRM 程式庫，則不應連結至 Wmvcore .lib。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

