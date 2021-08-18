---
description: 登錄資料表會保存應用程式必須在系統登錄中設定的登錄資訊。
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: 登錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b76fbc52357cdba68dfdcdda37e6edb3032086bf101788db0cdc69c0281264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128988"
---
# <a name="registry-table"></a>登錄資料表

登錄資料表會保存應用程式必須在系統登錄中設定的登錄資訊。

登錄資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 登錄    | [識別碼](identifier.md) | Y   | N        |
| Root        | [整數](integer.md)       | N   | N        |
| 答案         | [RegPath](regpath.md)       | N   | N        |
| 名稱        | [格式 化](formatted.md)   | N   | Y        |
| 值       | [格式 化](formatted.md)   | N   | Y        |
| 元件\_ | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>註冊 表
</dt> <dd>

用來識別登錄記錄的主要金鑰。

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>根
</dt> <dd>

登錄值的預先定義根金鑰。 在此欄位中輸入-1 的值，可讓根金鑰與安裝類型相依。 輸入下表中的其中一個值，以強制將登錄值寫入至特定根金鑰。



| 常數                          | 十六進位 | Decimal | 根金鑰                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (無)                            | \- 0x001    | -1      | 如果這是每一使用者的安裝，登錄值會以 **HKEY \_ CURRENT \_ user** 撰寫。 如果這是每部電腦的安裝，登錄值會寫入 **HKEY \_ 本機 \_ 電腦**。 請注意，您可以藉由將 [**ALLUSERS**](allusers.md) 屬性設定為1來指定每部電腦安裝。<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_在 \_ 安裝期間，安裝** 程式會在每個使用者 [安裝內容](installation-context.md)中，從 **HKCU \\ Software \\** class hive 寫入或移除值。<br/> 安裝程式會在每一部電腦安裝期間，寫入或移除 **HKLM \\ Software \\** class hive 中的值。<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ 目前的 \_ 使用者**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ 本機 \_ 電腦**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **HKEY \_ 使用者**                                                                                                                                                                                                                                                                                                                              |



 

請注意，建議寫入 **HKCU** hive 的登錄專案參考在 [元件資料表](component-table.md)的 [屬性] 資料行中設定 RegistryKeyPath 位的元件。 這可確保當相同電腦上有多個使用者時，安裝程式會寫入必要的登錄專案。

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

登錄值的可當地語系化金鑰。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

此資料行包含可當地語系化)  (的登錄值名稱。 如果這是 Null，則會將輸入到 [值] 資料行中的資料寫入預設的登錄機碼。

如果 [值] 資料行是 Null，則 [名稱] 資料行中的下表所示的字串會有特殊意義。



| String | 意義                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | 安裝元件時，就會建立金鑰（如果不存在）。                                                                                                                            |
| \-     | 卸載元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。                                                                                     |
| \*     | 安裝元件時，就會建立金鑰（如果不存在）。 此外，卸載元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。 |



 

請注意，安裝元件時，如果已安裝的登錄機碼具有其值和子機碼，就必須使用 [RemoveRegistry 資料表](removeregistry-table.md) 。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

此資料行是可當地語系化的登錄值。 此欄位已 [格式化](formatted.md)。 如果值附加至下列其中一個前置詞 (即 \# % *值*) 則會解讀此值，如表格中所述。 請注意，每個前置詞的開頭都是數位記號 (\#) 。 如果值的開頭為兩個以上的連續數位記號 (\#) ，則 \# 會忽略第一個，並將值轉譯並儲存為字串。



| 前置詞 | 意義                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#X    | 值會以十六進位值的形式加以解讀和儲存 (REG \_ BINARY) 。      |
| \#%    | 值會被解讀並儲存為可擴充的字串， (REG \_ EXPAND \_ SZ) 。 |
| \#     | 值會被解讀並儲存為整數 (REG \_ DWORD) 。                |



 

-   如果值包含序列波狀 \[ ~ \] 符號，則會將值解釋為以 Null 分隔的字串清單， (REG \_ 多重 \_ SZ) 。 例如，若要指定包含三個字串 a、b 和 c 的清單，請使用 "a \[ ~ \] b \[ ~ \] c"。
-   \[ ~ \] 值內的序列會分隔個別字串，並將其解釋並儲存為 Null 字元。
-   如果在 \[ ~ \] 字串清單之前，則字串會附加到任何現有的登錄值字串。 如果登錄值中已出現附加字串，則會移除字串的原始出現位置。
-   如果在 \[ ~ \] 字串清單結尾之後，字串就會加到任何現有的登錄值字串前面。 如果登錄值中已有前置字串，則會移除字串的原始出現位置。
-   如果 \[ ~ \] 是在開頭和結尾，或是字串清單的開頭或結尾都不是，則字串會取代任何現有的登錄值字串。
-   否則，值會以字串的形式來解讀和儲存 (REG \_ SZ) 。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵參考控制登錄值安裝的元件。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [WriteRegistryValues](writeregistryvalues-action.md)和 [RemoveRegistryValues](removeregistryvalues-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

當已選取要在本機安裝或從來源執行的對應元件時，系統會將登錄資訊寫出至系統登錄。

請注意，在移除機碼下的最後一個值或子機碼之後，安裝程式會移除登錄機碼。 若要避免在卸載時移除空白的登錄機碼，請在您需要保留的機碼底下寫入虛擬值，然後在 [名稱] 資料行中輸入 +。 如果 \* 是在 [名稱] 資料行中，當移除元件時，就會刪除該索引鍵及其所有值和子機碼。

自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄資料表。 這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。 因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。 自訂動作必須位於動作順序中的 [RemoveRegistryValues](removeregistryvalues-action.md) 和 [WriteRegistryValues](writeregistryvalues-action.md) 動作之前。

如需如何保護登錄機碼的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) 和 [LockPermissions 資料表](lockpermissions-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




