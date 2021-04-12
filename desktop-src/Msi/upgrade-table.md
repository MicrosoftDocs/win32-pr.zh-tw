---
description: 升級資料表包含主要升級期間所需的資訊。
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: 升級資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b48ce49f0f931209ccf472cd74b352c270353a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320560"
---
# <a name="upgrade-table"></a>升級資料表

升級資料表包含 [主要升級](major-upgrades.md)期間所需的資訊。 若要完全啟用安裝程式的升級功能，每個封裝都應該有 [**UpgradeCode**](upgradecode.md) 屬性和升級資料表。 升級資料表中的每一筆記錄都會提供升級程式碼、產品版本和語言資訊的特性組合，用來識別一組受升級影響的產品。 當 [FindRelatedProducts](findrelatedproducts-action.md) 動作偵測到安裝在系統上的受影響產品時，會將產品程式碼附加至 ActionProperty 資料行中指定的屬性。 [RemoveExistingProducts](removeexistingproducts-action.md)動作和[MigrateFeatureStates](migratefeaturestates-action.md)動作只會移除或遷移 ActionProperty 資料行中所列的產品。

升級資料表包含下表所示的資料行。



| Column         | 類型                         | 答案 | Nullable |
|----------------|------------------------------|-----|----------|
| UpgradeCode    | [GUID](guid.md)             | Y   | N        |
| VersionMin     | [Text](text.md)             | Y   | Y        |
| VersionMax     | [Text](text.md)             | Y   | Y        |
| 語言       | [Text](text.md)             | Y   | Y        |
| 屬性     | [整數](integer.md)       | Y   | N        |
| 移除         | [格式 化](formatted.md)   | N   | Y        |
| ActionProperty | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode
</dt> <dd>

此資料行中的 [UpgradeCode](upgradecode.md) 屬性會指定 [FindRelatedProducts](findrelatedproducts-action.md) 動作要偵測的所有產品的升級程式碼。

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin
</dt> <dd>

[FindRelatedProducts](findrelatedproducts-action.md)所偵測到的產品版本範圍下限。 在 [屬性] 中輸入 **msidbUpgradeAttributesVersionMinInclusive** ，以包含範圍內的 VersionMin。 如果 VersionMin 等於空字串 ( "" ) 它會評估為與0相同。 如果 VersionMin 為 null，FindRelatedProducts 會忽略 **msidbUpgradeAttributesVersionMinInclusive** 並偵測所有先前的版本。 VersionMin 和 VersionMax 不得同時為 null。

VersionMin 必須是有效的產品版本，如 [**ProductVersion**](productversion.md) 屬性所述。 請注意，Windows Installer 只會使用產品版本的前三個欄位。 如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax
</dt> <dd>

[FindRelatedProducts](findrelatedproducts-action.md)動作所偵測到之產品版本範圍的上限。 在 [屬性] 中輸入 **msidbUpgradeAttributesVersionMaxInclusive** ，以包含範圍內的 VersionMax。 如果 VersionMax 是 ( "" ) 的空字串，則會評估為與0相同。 如果 VersionMax 為 null，FindRelatedProducts 會忽略 **msidbUpgradeAttributesVersionMaxInclusive** ，並偵測大於 (或大於或等於) VersionMin 和 **msidbUpgradeAttributesVersionMinInclusive** 指定之下限的所有產品版本。 VersionMin 和 VersionMax 不得同時為 null。

VersionMax 必須是有效的產品版本，如 [**ProductVersion**](productversion.md) 屬性所述。 請注意，Windows Installer 只會使用產品版本的前三個欄位。 如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

[FindRelatedProducts](findrelatedproducts-action.md)偵測到的語言集合。 輸入數位語言識別項的清單 (LANGID) 以逗號分隔。 在 [屬性] 中輸入 **msidbUpgradeAttributesLanguagesExclusive** ，以偵測語言中列出的所有語言。 如果 Language 為 null 或空字串 ( "" ) ，FindRelatedProducts 會忽略 **msidbUpgradeAttributesLanguagesExclusive** 並偵測所有語言。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

此資料行包含指定升級資料表之屬性的位旗標。



| 位旗標名稱                                 | Decimal | 十六進位 | 屬性                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | 藉由啟用 [MigrateFeatureStates](migratefeaturestates-action.md) 動作中的邏輯來遷移功能狀態。 |
| **msidbUpgradeAttributesOnlyDetect**          | 2       | 0x002       | 偵測產品和應用程式，但不會移除。                                                               |
| **msidbUpgradeAttributesIgnoreRemoveFailure** | 4       | 0x004       | 在無法移除產品或應用程式時，繼續安裝。                                              |
| **msidbUpgradeAttributesVersionMinInclusive** | 256     | 0x100       | 偵測版本的範圍，包括 VersionMin 中的值。                                                     |
| **msidbUpgradeAttributesVersionMaxInclusive** | 512     | 0x200       | 偵測版本的範圍，包括 VersionMax 中的值。                                                     |
| **msidbUpgradeAttributesLanguagesExclusive**  | 1024    | 0x400       | 偵測語言資料行中所列語言以外的所有語言。                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>刪除
</dt> <dd>

安裝程式會將 [ [**移除**](remove.md) ] 屬性設定為此資料行中指定的功能。 您可以在執行時間判斷要移除的功能。 在此欄位中輸入的 [格式化](formatted.md) 字串必須評估為功能名稱的逗號分隔清單。 例如： \[ Feature1 \] 、 \[ Feature2 \] 、 \[ Feature3 \] 。 如果欄位包含的格式化文字會評估為空字串 ( "" ) ，則不會移除任何功能。 只有當 [移除] 欄位是空的時，安裝程式才會設定 REMOVE = ALL。 請注意空字串與空白欄位之間的差異。 如果欄位是空的，則為 null。

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty
</dt> <dd>

當 [FindRelatedProducts](findrelatedproducts-action.md) 動作偵測到安裝在系統上的相關產品時，會將產品程式碼附加至此欄位中指定的屬性。 在此資料行中指定的屬性必須是公用屬性，而且封裝作者必須將屬性加入至 [**SecureCustomProperties**](securecustomproperties.md) 屬性。 升級資料表中的每個資料列都必須有唯一的 ActionProperty 值。 FindRelatedProducts 之後，此屬性的值為清單產品代碼，並以分號分隔 (; ) ，在系統上偵測到。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 



