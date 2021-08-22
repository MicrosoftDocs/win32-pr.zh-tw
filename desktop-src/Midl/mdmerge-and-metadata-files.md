---
title: MDMERGE 和中繼資料檔案
description: 根據命名空間，將多個中繼資料 ( winmd) 檔案組成多個輸出中繼資料檔案。
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- 中繼資料
- winmd 檔案
- Windows 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252428"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE 和中繼資料檔案

根據命名空間，將多個中繼資料 ( winmd) 檔案組成多個輸出中繼資料檔案。

## <a name="usage"></a>使用量

使用下列命令，從命令列執行 MDMERGE：

**mdmerge**  *<***選項**_>_

where * < ***options** _>_ 代表您要使用的命令列選項。

使用 midlrt.exe 根據編譯器產生自訂 Windows 執行階段元件的中繼資料檔案。 如需詳細資訊，請參閱[midlrt.exe 根據和 Windows 執行階段元件](midlrt-and-windows-runtime-components.md)。

## <a name="command-line-switches"></a>命令列參數

下列清單顯示 MDMERGE 使用的命令列參數。

<dl>

[**/i**](-mdmerge-i.md)  
[**/metadata \_ 目錄**](-mdmerge-metadata-dir.md)  
[**n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

當您使用 **-h** 和 **/？** 時，可使用 MDMERGE 編譯器參數和選項的完整清單。 開關。

## <a name="remarks"></a>備註

中繼資料組合可讓多個 IDL 檔案包含相同命名空間中 Windows 執行階段元件的定義。 這可讓您無法在單一 IDL 檔案內的命名空間中定義所有類型。

您的應用程式所使用的 Windows 執行階段元件可能很多。 當您執行最後一個步驟來產生可部署的 Windows 執行階段中繼資料元件時，您可以將 MDMERGE 設定為合併多個中繼資料目錄中的元件，例如與系統一起安裝的元件 (% Windows% \\ system32 \\ WinMetadata) 、您的基礎類型，以及目前專案的組建目錄。 所有必要的類型都會合並到正確、可部署的中繼資料元件中，您可以為 Windows 存放區封裝。

您可以使用 [**/n**](-mdmerge-n.md) 選項來指定所支援的命名空間深度，以撰寫中繼資料元件。 這可讓您設定 Windows 執行階段元件的熱分割，因此只會封裝單一的 winmd 檔案，而不是多個檔案。 這可減少您 Windows 存放區應用程式所需的載入時間和檔案 i/o。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[midlrt.exe 根據和 Windows 執行階段元件](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




