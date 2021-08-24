---
description: ICE61 會驗證 Windows Installer 資料庫的升級資料表。
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c772a076decaa385d01047daa45871aeeaf7898d4cf3347606c4066d1f7f2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580978"
---
# <a name="ice61"></a>ICE61

ICE61 會檢查升級資料表，以確定下列條件成立：

-   所有 ActionProperty 屬性都不是在屬性工作表中預先撰寫的。
-   所有 ActionProperty 屬性都是公用屬性。
-   所有 ActionProperty 屬性都包含在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中。
-   所有 ActionProperty 屬性對升級資料表中的每一筆記錄而言是唯一的。
-   所有 VersionMax 值都不小於對應的 VersionMin 值。
-   VersionMin 和 VersionMax 值都是有效的產品版本。 如需有效的產品版本格式，請參閱 [**ProductVersion**](productversion.md) 屬性。
-   不嘗試移除目前產品的較新或相同版本。

若無法修正 ICE61 回報的警告或錯誤，通常會導致升級應用程式時發生問題。 視確切的錯誤而定，這可能是因為新的應用程式需要離開舊版本的檔案、從較舊版本刪除檔案，或升級完成失敗的任何事項。

## <a name="result"></a>結果

如果上述任何條件不成立，ICE61 會張貼警告或錯誤。

## <a name="example"></a>範例

ICE61 會針對所顯示的範例報告下列錯誤和警告。

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

在此情況下，第一個資料列會嘗試移除相同版本的產品。  (的 VersionMax 資料行等於屬性工作表) 中的產品版本。

若要修正這個錯誤，請使用 VersionMax 資料行中的版本低於屬性工作表中指定的目前版本。 如果 VersionMax 等於目前的版本，請從 [屬性] 資料行中移除 **msidbUpgradeAttributesVersionMaxInclusive** 位。 如果目的只是要偵測產品而不移除它，則將 **msidbUpgradeAttributesOnlyDetect** 位新增至 [屬性] 欄也會修正這個錯誤。

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

除非在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中列出屬性，否則在找到屬性時，不會將屬性傳遞至安裝的伺服器端。

若要修正這個錯誤，請將屬性新增至 [**SecureCustomProperties**](securecustomproperties.md)。

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

升級屬性必須是公用屬性，才能將結果傳遞給安裝的伺服器端。

若要修正這個錯誤，請在屬性名稱中使用所有大寫字母。

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

屬性只能用於升級資料表的一個資料列。

若要修正這個錯誤，請針對第二個數據列使用不同的屬性。

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

最小版本必須小於最大版本。

若要修正這個錯誤，請檢查您的版本號碼是否出現錯誤。 如果是正確的，而且您想要使用兩個版本之間的範圍，請將它們切換成使 VersionMin 小於 VersionMax。

[屬性工作表](property-table.md)



| 屬性                                                 | 值                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[升級資料表](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | 語言 | 屬性 | 移除                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



