---
description: 產生修補程式套件的建議方法是使用修補程式建立工具，例如 Msimsp.exe 和 Patchwiz.dll。 Msimsp.exe 工具僅適用于 Windows Installer 開發人員 Windows SDK 元件。
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa82f2fbefc9046877f4f98cf4a3c126d94e6542b60076f0491bd0f311ee00a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627795"
---
# <a name="msimspexe"></a>Msimsp.exe

產生修補程式套件的建議方法是使用修補程式建立工具，例如 Msimsp.exe 和 [Patchwiz.dll](patchwiz-dll.md)。 Msimsp.exe 工具僅適用于[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

Msimsp.exe 是呼叫 [Patchwiz.dll](patchwiz-dll.md)的可執行檔。 此工具可用來建立修補程式套件，方法是將路徑傳遞至 patch 建立屬性檔 ( pcp 檔案) ，以及要建立之修補程式套件的路徑。 Msimsp 也可以用來建立記錄檔，並指定暫存資料夾，以儲存用來建立修補程式套件的轉換、封包和檔案。

Msimsp.exe 的命令列語法為：

*\[ Pcp \]* 檔案的 **Msimsp.exe s** 路徑- *\[ .msp \]* 檔案 **的 p** 路徑 **{options}**

命令列選項不區分大小寫，而且可以使用斜線分隔符號，而不是虛線。 如果未指定任何選項，Msimsp.exe 會顯示摘要資訊屬性目前的值。

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s 的**_\[ \] pcp 檔案路徑_
</dt> <dd>

這是必要的，其後必須接著修補程式建立屬性檔的路徑 ( pcp 副檔名) 。 如需詳細資訊，請參閱 [PatchWiz.dll](patchwiz-dll.md)。

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-**_指向 .msp_ 檔案的 p 路徑
</dt> <dd>

這是必要的，且後面接著 ( .msp 延伸模組) 所建立修補套件的路徑。

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-**_暫存資料夾_ 的 f 路徑
</dt> <dd>

選擇性。 後面接著暫存資料夾的路徑。 預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

選擇性。 如果暫存資料夾已存在，則會失敗。

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_記錄_ 檔的路徑
</dt> <dd>

選擇性。 後面接著記錄檔的路徑，說明修補程式建立程式和錯誤。 如需詳細資訊，請參閱 UiCreatePatchPackage 的傳回 [值](return-values-for-uicreatepatchpackage.md)。

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-**_具有效能資料之記錄_ 檔的 lp 路徑
</dt> <dd>

選擇性。 後面接著記錄檔的路徑，說明修補程式建立程式和錯誤。 此選項會將效能資料寫入至記錄檔。 此選項需要4.0 版的 Patchwiz.dll。

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d.ddd...e**
</dt> <dd>

選擇性。 如果修補程式建立順利完成，則會顯示對話方塊。

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

顯示命令列說明。

</dd> </dl>

> [!Note]
> 如果安裝 [套件的檔案](file-table.md) 資料行中有值只有大小寫不同，Msimsp.exe 可能會在呼叫 Makecab.exe 時失敗。 Windows安裝程式會區分大小寫，而且只有在 Comp1 和 Comp2 安裝到不同的目錄時，才允許安裝封裝（例如下表中的表格）。 不過，在此案例中，您無法使用 Msimsp.exe 或 [Patchwiz.dll](patchwiz-dll.md) 來產生封裝的修補程式，因為 Msimsp.exe 和 Patchwiz.dll 呼叫不區分大小寫的 Makecab.exe。
> 
> 避免撰寫安裝套件，例如下列部分檔案 [資料表](file-table.md)。
> 
> | 檔案       | 元件\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立修補程式套件](creating-a-patch-package.md)
</dt> <dt>

[小型更新修補範例](a-small-update-patching-example.md)
</dt> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



