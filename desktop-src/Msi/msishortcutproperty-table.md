---
description: MsiShortcutProperty 資料表可讓 Window Installer 設定也是 Windows Shell 物件的快捷方式屬性。
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: MsiShortcutProperty 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513860"
---
# <a name="msishortcutproperty-table"></a>MsiShortcutProperty 資料表

MsiShortcutProperty 資料表可讓 Window Installer 設定也是 [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) 物件的快捷方式屬性。 從 Windows Vista 和 Windows Server 2008 開始，Windows Shell 會為 Shell 物件（例如快速鍵）提供 IPropertyStore 介面。 安裝快捷方式時，在 Windows Server 2008 R2 或 Windows 7 上執行的 Windows Installer 5.0 套件可以設定這些屬性。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用此資料表。

MsiShortcutProperty 資料表具有下列資料行。



| Column              | 類型                         | 答案 | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [識別碼](identifier.md) | Y   | N        |
| 快速鍵\_          | [識別碼](identifier.md) | N   | N        |
| PropertyKey         | [格式 化](formatted.md)   | N   | N        |
| PropVariantValue    | [格式 化](formatted.md)   | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

MsiShortcutProperty 資料表中這個資料列的唯一識別碼。

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>快捷方式\_
</dt> <dd>

[快速鍵](shortcut-table.md)資料表中的索引鍵，識別具有屬性集的快捷方式。

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

提供 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構資訊的字串值。 此欄位中的資訊必須參考以 Windows 屬性系統註冊之屬性的標準名稱。 如需 Windows 屬性系統的詳細資訊，請參閱 [屬性系統總覽](/previous-versions//bb776909(v=vs.85))。

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

提供 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構資訊的字串值。

</dd> </dl>

在快捷方式上可以設定多個屬性。 如果相同的快捷方式上已多次設定相同的屬性，則會以未指定的順序來設定值。

Windows Installer 只有在已安裝或重新安裝快捷方式時，才能設定快速鍵屬性。 未重新安裝已安裝之快捷方式的修補程式不會更新快捷方式的屬性。 Patch 可以藉由在修補程式套件中加入 [快捷方式](shortcut-table.md) 表，並重新安裝快捷方式來更新屬性。

## <a name="remarks"></a>備註

[Windows Installer 錯誤訊息](windows-installer-error-messages.md) 1946 會以警告傳回，而且如果 Windows Installer 無法設定 MsiShortcutProperty 資料表中指定的快捷方式屬性，則會繼續安裝。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
</dl>

 

 
