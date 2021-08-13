---
description: MsiAssembly 資料表會指定 Microsoft .NET Framework 元件和 Win32 元件的 Windows Installer 設定。 如需詳細資訊，請參閱將元件安裝到全域組件快取和 Win32 元件的安裝。
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: MsiAssembly 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda246bd6baba75d0f7e8d53f515a25abb0c163c2d3ef0b1b9705c123b8e69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381378"
---
# <a name="msiassembly-table"></a>MsiAssembly 資料表

MsiAssembly 資料表會指定 Microsoft .NET Framework 元件和 Win32 元件的 Windows Installer 設定。 如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。

在 Windows XP 上，Windows Installer 可以安裝 Win32 元件作為[並存元件](side-by-side-assemblies.md)。 如需詳細資訊，請參閱 [並存元件 API](../sbscs/side-by-side-assembly-api.md)。

**Windows 2000：** 這項功能不受支援。

MsiAssembly 資料表具有下列資料行。



| Column            | 類型                         | 答案 | Nullable |
|-------------------|------------------------------|-----|----------|
| 元件\_       | [識別碼](identifier.md) | Y   | N        |
| 特徵\_         | [識別碼](identifier.md) | N   | N        |
| 檔案 \_ 資訊清單    | [識別碼](identifier.md) | N   | Y        |
| 檔 \_ 應用程式 | [識別碼](identifier.md) | N   | Y        |
| 屬性        | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)中的索引鍵，指定包含此元件的 Windows Installer 元件。

此欄位中的值不得設定為 null。 [元件資料表](component-table.md)中的元件 KeyPath 欄位不得為 null。

針對 Win32 元件，元件 KeyPath 不能是檔案資訊清單中指定的資訊清單檔 \_ 。 資訊清單可以是 .NET Framework 或原則元件的 keypath。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

[功能資料表](feature-table.md)中的索引鍵。

當功能安裝必須安裝元件時，Windows Installer 會安裝這個欄位所指向的功能。

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>檔案 \_ 資訊清單
</dt> <dd>

檔案[資料表](file-table.md)中的外部索引鍵，指定包含 .NET Framework 元件或 Win32 元件之資訊清單的檔案。

若為 Win32 元件，請勿在 [元件資料表](component-table.md)的 [KeyPath] 欄位中，將此檔案指定為元件金鑰路徑檔案。

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>檔 \_ 應用程式
</dt> <dd>

若要在私用位置安裝元件，請在此欄位中輸入元件元件的金鑰路徑檔案。

這是出現在 [元件資料表](component-table.md)的 KeyPath 欄位中的值。 然後，安裝程式可以將元件安裝到 [目錄資料表](directory-table.md)中所指定之元件的目錄結構。 如果要將元件安裝到全域組件快取中，這個欄位必須是 null。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

輸入 1 (一個 Win32 元件的) 值。 輸入 .NET Framework 元件的值為 0 (零) 。

如果 [屬性] 資料行是 Null，則安裝程式會將元件視為 .NET Framework 元件。

</dd> </dl>

## <a name="remarks"></a>備註

如果 MsiAssembly 資料表中至少有一個專案，則 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 必須包含 [MsiPublishAssemblies 動作](msipublishassemblies-action.md)和 [MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md)。

因為元件無法在認可之後復原，Windows Installer 會使用兩步驟的安裝程式。 元件的介面是在 [MsiPublishAssemblies 動作](msipublishassemblies-action.md)所產生的安裝作業期間建立。

在成功執行 [InstallFinalize 動作](installfinalize-action.md)之前，不會認可這些元件。 這表示，如果您撰寫相依元件的自訂動作或資源，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序。 例如，如果您需要啟動相依于全域組件快取中元件 (GAC) 的服務，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排程該服務的啟動。 這表示您無法使用 [ServiceControl 資料表](servicecontrol-table.md) 來啟動服務，而是必須使用在 InstallFinalize 之後排序的自訂動作。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
