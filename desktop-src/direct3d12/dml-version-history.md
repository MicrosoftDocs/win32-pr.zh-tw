---
title: DirectML 版本歷程記錄
description: DirectML 是以 Windows 10 的系統元件的形式來散發，並可作為 Windows 10 作業系統 (OS) 版本 1903 Windows 10 10.0;組建 18362) 和更新版本。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 0a2524faf077b6e4198810395e4aef8da56780af
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282567"
---
# <a name="directml-version-history"></a>DirectML 版本歷程記錄

DirectML 是以 Windows 10 的系統元件的形式來散發，並可作為 Windows 10 作業系統 (OS) 版本 1903 Windows 10 10.0;組建 18362) 和更新版本。

從 DirectML 版本1.4.0 開始，DirectML 也可做為獨立的可轉散發套件， (查看[DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)) ，此功能適用于想要使用固定版本 DirectML 的應用程式，或在舊版 Windows 10 上執行時。

DirectML 遵循 [語義版本](https://semver.org/) 設定慣例。 亦即，版本號碼會遵循表單 `major.minor.patch` 。 DirectML 的第一個版本有1.0.0 版。

## <a name="version-table"></a>版本資料表

|DirectML 版本|支援的功能層級 (參閱 [DirectML 功能層級歷程記錄](./dml-feature-level-history.md)) |DML_TARGET_VERSION|首次提供| (可轉散發套件中的第一版) |
|-|-|-|-|-|
|1.6.0|DML_FEATURE_LEVEL_4_0|`0x4000`|N/A|[DirectML-1.6。0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.6.0)|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|N/A|[DirectML-1.5。0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/A|[DirectML-1.4。0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10，版本 2004 (10.0;組建 19041)  (Windows 10 2020 Update) 。 也稱為「20H1」。|N/A|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10，版本 1903 (10.0;組建 18362)  (Windows 10 2019 年5月更新) 。 也稱為「19H1」。|N/A|

<sup>1</sup> 1.2.0 和1.3.0 中繼版本的 DirectML 未提供廣泛的支援。

## <a name="selecting-a-directml-target-version"></a>選取 DirectML 目標版本

為了方便起見，標頭檔中的某些功能 `DirectML.h` 會根據宏的值，有條件地宣告 `DML_TARGET_VERSION` 。 藉由將 `DML_TARGET_VERSION` 宏設定為特定值，您可以 `DirectML.h` 從應用程式中排除的部分。

如果您使用較新的 `DirectML.h` 版本，但您的目標是較低版本的 DirectML 二進位檔，這會很有説明，因為它可確保任何嘗試使用所選目標層以外的功能都不會進行編譯。 這個機制類似于 `NTDDI_VERSION` 宏 (請參閱) [條件式宣告的宏](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations) 。

以下是宏的有效值 `DML_TARGET_VERSION` 。

|DML_TARGET_VERSION|效果|
|-|-|
|`0x4000`|任何需要比 **1.6.0** 更新之 DirectML 版本的功能，都將從中排除 `DirectML.h` 。|
|`0x3000`|任何需要比 **1.4.0** 更新之 DirectML 版本的功能，都將從中排除 `DirectML.h` 。|
|`0x2000`|任何需要比 **1.1.0** 更新之 DirectML 版本的功能，都將從中排除 `DirectML.h` 。|
|`0x1000`|任何需要比 **1.0.0** 版 DirectML 更新的功能都會從排除 `DirectML.h` 。|
|*未設定*|系統會自動為您選取目標版本。 如需詳細資料，請參閱下文。|

如果 `DML_TARGET_VERSION` 未設定，則會自動選取它，如下所示。

* 如果已 `DML_TARGET_VERSION_USE_LATEST` 定義宏，則會選取最新的目標版本。
* 否則，會根據宏的值選取目標版本 `NTDDI_VERSION` 。
  *  `NTDDI_WIN10_CO` 產生的目標版本 `0x4000` 。
  *  `NTDDI_WIN10_FE` 產生的目標版本 `0x3000` 。
  *  `NTDDI_WIN10_VB` 產生的目標版本 `0x2000` 。
  *  `NTDDI_WIN10_19H1` 產生的目標版本 `0x1000` 。
  *  如果 `NTDDI_VERSION` 未定義，則會選取最新的目標版本， (如同 `DML_TARGET_VERSION_USE_LATEST`) 指定。

### <a name="example"></a>範例

請考慮使用版本 10.0.19041.0 (Windows 10，Windows 軟體開發套件 (SDK) 版本 2004) 的應用程式。 從上表中，這個對應的 DirectML 版本是1.1.0，而對應的 `DML_TARGET_VERSION` 是 `0x2000` 。

如果您未設定 `DML_TARGET_VERSION` 或 `NTDDI_VERSION` 宏，則選取的目標版本將預設為 `0x2000` ，而且中的所有專案都可供 `DirectML.h` 使用。

如果您想要讓應用程式能夠在 Windows 10 上執行，1903版 (10.0;組建 18362) ，然後您就可以 `#define DML_TARGET_VERSION 0x1000` 將 `DirectML.h` DirectML 1.0.0 版不支援的所有內容排除在其中。 這可確保任何嘗試使用需要較高版本之功能的嘗試都將無法編譯。

## <a name="directml-version-versus-feature-level"></a>DirectML 版本與功能等級

DirectML 版本 (例如，1.0.0 或 1.4.0) 說明特定版本的 DirectML，包括其相關聯的 `DirectML.h` 標頭檔和檔案 `.lib` 。

例如，或) 的功能層級 (`DML_FEATURE_LEVEL_1_0` `DML_FEATURE_LEVEL_2_0` 描述 API 基礎執行的功能，這可能會因使用的版本而異 `DirectML.h` 。

例如，針對較新的 sdk 所建立，但在舊版 Windows 上執行的應用程式，在執行時間可能 () 查看較低支援的功能層級，即使是針對最新的 sdk 進行編譯也一樣。

## <a name="see-also"></a>另請參閱

* [DirectML 功能等級歷程記錄](./dml-feature-level-history.md)
* [DML_FEATURE_LEVEL 列舉](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [DirectML 可轉散發套件](https://www.nuget.org/packages/Microsoft.AI.DirectML/)