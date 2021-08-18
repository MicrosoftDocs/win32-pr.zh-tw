---
description: REINSTALLMODE 屬性是一個字串，其中包含指定要執行之重新安裝類型的字母。
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 227a069fa0974758bf623c83ef23d40902d9feb140f69446c57c2d723468054f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637874"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE 屬性

**REINSTALLMODE** 屬性是一個字串，其中包含指定要執行之重新安裝類型的字母。 選項不區分大小寫，且順序無關。 這個屬性通常一律會與 [**重新安裝**](reinstall.md) 屬性搭配使用。 不過，在安裝期間也可以使用這個屬性，而不只是重新安裝。

> [!Note]  
> Windows Installer 會在 [系統管理安裝](administrative-installation.md)期間忽略 **REINSTALLMODE** 屬性。

 

## <a name="reinstall-option-codes"></a>重新安裝選項代碼

依預設， **REINSTALLMODE** 為 "omus reinstall"。



| 程式碼 | 選項                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | 只有在檔案遺失時才重新安裝。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | 如果檔案遺失或較舊的版本，請重新安裝。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | 如果檔案遺失或相同或較舊的版本，請重新安裝。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | 如果檔案遺失或有不同的版本，請重新安裝。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | 確認總和檢查碼值，如果檔案遺失或損毀，請重新安裝。 此旗標只會修復檔案 [資料表](file-table.md)的 [屬性] 資料行中有 msidbFileAttributesChecksum 的檔案。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | 無論總和檢查碼或版本為何，都強制重新安裝所有檔案。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | 從登錄 [資料表](registry-table.md) 中，將所有必要的登錄專案重新寫入至 **HKEY \_ 目前 \_ 使用者**<br/> 或 **HKEY \_ 使用者**<br/> 登錄 hive。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | 從移至 **HKEY \_ 本機 \_ 電腦** 的登錄 [資料表](registry-table.md)重寫所有必要的登錄專案<br/> 或 **HKEY \_ 類別 \_ 根目錄**<br/> 登錄 hive。 從 [類別資料表](class-table.md)、 [動詞資料表](verb-table.md)、 [PublishComponent 資料表](publishcomponent-table.md)、 [ProgID 資料表](progid-table.md)、 [MIME 資料表](mime-table.md)、 [圖示資料表](icon-table.md)、 [延伸資料表](extension-table.md)和 [AppID 資料表](appid-table.md) 重寫所有資訊，而不論電腦或使用者指派為何。 重新安裝所有 [**合格元件。**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)重新安裝應用程式時，此選項會執行 [RegisterTypeLibraries](registertypelibraries-action.md) 和 [InstallODBC](installodbc-action.md) 動作。<br/> |
| s    | 重新安裝所有的快捷方式，並重新快取所有圖示，以覆寫任何現有的快捷方式和圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | 使用從來源套件執行，然後重新快取本機封裝。 在第一次安裝應用程式或功能時，請勿使用 v 重新安裝選項程式碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

如果定義 **REINSTALLMODE** 屬性時未同時定義 [**重新安裝**](reinstall.md) 內容，則仍會套用指定的「偵測」模式，並指定一般安裝的「覆寫」模式。 **REINSTALLMODE** 屬性只會影響一般為安裝所選取的功能。 **REINSTALLMODE** 屬性的存在並不會重新安裝功能。 重新安裝功能需要 **重新安裝** 屬性。

這個屬性的選項代碼會對應至 [命令列選項](command-line-options.md) '/f '。 命令列選項的預設值為 ' pecms '。

> [!Note]  
> 只會驗證並修復包含總和檢查碼資訊的檔案。 \_上述 ccode (的 REINSTALLMODE FILEVERIFY 旗標) 只會修復檔案[資料表](file-table.md)之 [屬性] 資料行中具有 msidbFileAttributesChecksum 的檔案。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




