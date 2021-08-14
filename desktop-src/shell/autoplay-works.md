---
description: 建立啟用自動啟用的應用程式是一個簡單的程式。 本主題使用 CD-ROM 作為範例 (它是執行這項技術的第一個媒體) 但現今有許多不同的媒體類型可以使用它。
title: 建立 AutoRun-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f3a3c265f71b0bdf66d7825e65eb69ab975bfc6bffa5c9a8674ed5a0fb8feb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224930"
---
# <a name="creating-an-autorun-enabled-application"></a>建立 AutoRun-Enabled 應用程式

建立啟用自動啟用的應用程式是一個簡單的程式。 本主題使用 CD-ROM 作為範例 (它是執行這項技術的第一個媒體) 但現今有許多不同的媒體類型可以使用它。

若要在您的應用程式中啟用自動執行，您只需要包含兩個基本的檔案：

-   自動運行的 .inf 檔案
-   啟動應用程式

當使用者將光碟插入與自動執行相容的電腦上的 CD-ROM 光碟機時，系統會立即檢查光碟是否有個人電腦檔案系統。 如果有的話，系統會搜尋名為「 [自動執行 .inf](#creating-an-autoruninf-file)」的檔案。 此檔案會指定要執行的安裝應用程式，以及各種選擇性的設定。 啟動應用程式通常會安裝、卸載、設定，而且可能會執行應用程式。

-   [建立自動播放 .inf 檔案](#creating-an-autoruninf-file)
-   [\[DeviceInstall \] 區段](#the-deviceinstall-section)
-   [相關主題](#related-topics)

## <a name="creating-an-autoruninf-file"></a>建立自動播放 .inf 檔案

[自動安裝] 是位於 cd-rom 根目錄的文字檔，其中包含您的應用程式。 其主要功能是為系統提供應用程式啟動程式的名稱和位置，在插入光碟時將會執行此程式。

> [!Note]  
> \_從 [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)傳回磁片磁碟機的磁片磁碟機，在 Windows XP 下不支援自動運行 .inf 檔案。

 

自動執行 .inf 檔案也可以包含選用的資訊，包括：

-   包含圖示的檔案名，該圖示代表您應用程式的 CD-ROM 光碟機。 Windows 檔案總管取代標準磁片磁碟機圖示時，會顯示此圖示。
-   當使用者以滑鼠右鍵按一下 CD-ROM 圖示時，所顯示之快捷方式功能表的其他命令。 您也可以指定當使用者按兩下圖示時，所執行的預設命令。

自動運行的 .inf 檔案類似于 .ini 檔案。 它們是由一或多個區段所組成，每個區段都是以方括弧括住的名稱。 每個區段都包含一系列的命令，這些命令會在插入光碟時由 Shell 執行。 目前有兩個區段是針對自動播放的 .inf 檔案所定義。

-   [ **\[ 自動 \] 運行**] 區段包含預設的自動運行命令。 所有自動運行的 .inf 檔案都必須有 [ **\[ 自動運行 \]** ] 區段。
-   選擇性的 [自動執行] **\[ Alpha \]** 區段可包含在 RISC 型電腦上執行的系統中。 將光碟插入至 RISC 型系統的 CD-ROM 光碟機時，Shell 會執行本節中的命令，而不是 [ **\[ 自動 \]** 執行] 區段中的命令。

> [!Note]  
> Shell 會先檢查特定的架構區段。 如果找不到，則會使用 [ **\[ 自動 \]** 執行] 區段中的資訊。 當 Shell 找到某個區段之後，它會忽略所有其他區段，因此每個區段都必須是獨立的。

 

每一節都包含一系列的命令，用來決定自動執行時間的運作方式。 有五個可用的命令。



| 命令                         | 描述                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [defaulticon](autorun-cmds.md) | 指定應用程式的預設圖示。                                        |
| [圖示](autorun-cmds.md)        | 指定 CD-ROM 光碟機的應用程式特定圖示的路徑和檔案名。 |
| [open](autorun-cmds.md)        | 指定啟動應用程式的路徑和檔案名。                           |
| [useautorun](autorun-cmds.md)  | 指定如果支援，則應使用自動播放 V2 功能。                       |
| [殼](autorun-cmds.md)       | 在 CD-ROM 的快捷方式功能表中定義預設命令。                             |
| [shell \_ 動詞](autorun-cmds.md) | 將命令新增至 CD-ROM 的快捷方式功能表。                                           |



 

以下是簡單的自動執行 .inf 檔案範例。 它會將 Filename.exe 指定為啟動應用程式。 Filename.exe 中的第二個圖示將表示 CD-ROM 光碟機，而不是標準磁片磁碟機圖示。


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



這個自動執行 .inf 範例會根據電腦的類型，執行不同的啟動應用程式。


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>\[DeviceInstall \] 區段

您可以使用任何卸載式媒體上的 **\[ DeviceInstall \]** 區段。 只有在 Windows XP 下才支援此功能。 您可以使用 **DriverPath** 來指定 Windows XP 搜尋驅動程式檔案的目錄路徑，以避免長時間搜尋整個內容。

您可以使用 **\[ DeviceInstall \]** 區段和驅動程式安裝來指定目錄，其中 Windows XP 應該在媒體上搜尋驅動程式檔案。 在 Windows XP 下，預設不會再搜尋整個媒體，因此需要 **\[ DeviceInstall \]** 指定搜尋位置。 以下是唯一 Windows XP 完整搜尋的卸載式媒體，而不需要在執行 .inf 檔案中 **\[ DeviceInstall \]** 區段。

-   磁片磁碟機 A 或 B 中找到的磁片。
-   CD/DVD 媒體的大小不會超過 1 gb (GB) 。

所有其他媒體都必須包含 **\[ DeviceInstall \]** 區段，才能讓 Windows XP 偵測儲存在該媒體上的任何驅動程式。

> [!Note]  
> 如同 [ **\[ 自動運行 \]** ] 區段， **\[ DeviceInstall \]** 區段可以是架構專屬的。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何執行自動啟動應用程式](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[撰寫裝置安裝應用程式](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
