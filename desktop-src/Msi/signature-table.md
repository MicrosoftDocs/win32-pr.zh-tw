---
description: 簽章資料表會保存唯一識別檔案簽章的資訊。 如需有關簽章的詳細資訊，請參閱數位簽章和 Windows Installer。
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: 簽名表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987227"
---
# <a name="signature-table"></a>簽名表

簽章資料表會保存唯一識別檔案簽章的資訊。 如需有關簽章的詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。

簽章資料表具有下列資料行。



| Column     | 類型                               | 答案 | Nullable |
|------------|------------------------------------|-----|----------|
| 簽名  | [識別碼](identifier.md)       | Y   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | Y        |
| Odata-maxversion | [Text](text.md)                   | N   | Y        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MinDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| 語言  | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名
</dt> <dd>

簽章資料行是唯一的檔案簽章。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

檔案的名稱。

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

檔案的最小版本，使用語言比較。 如果指定此欄位，則檔案的版本必須至少等於 MinVersion。 如果檔案的版本等同于 MinVersion 域值，但 [語言] 資料行中指定的語言不同，則檔案不會滿足簽章篩選準則。

> [!Note]  
> 在比較中使用語言資料行中指定的語言，而且沒有任何方法可忽略語言。 如果您希望檔案符合 MinVersion 欄位需求（不論語言為何），您必須在 [MinVersion] 欄位中輸入一個小於實際值的值。 例如，如果篩選的最小版本是2.0.2600.1183，請使用2.0.2600.1182 來尋找檔案，但不符合語言資訊。

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>Odata-maxversion
</dt> <dd>

檔案的最大版本。 如果指定此欄位，則檔案的版本必須最等於 Odata-maxversion。

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

檔案的大小下限。 如果指定此欄位，則檢查中的檔案必須具有至少等於 MinSize 的大小。 此值必須是非負數。

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize
</dt> <dd>

檔案的大小上限。 如果指定此欄位，則檢查中的檔案必須具有最等於 MaxSize 的大小。 此值必須是非負數。

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

檔案的最小修改日期和時間。 如果指定此欄位，則檢查中的檔案必須具有至少等於 MinDate 的修改日期和時間。 此值必須是非負數。 此欄位的格式為 " **WORD**" 類型的兩個壓縮的16位值。 高序位 **單字** 值會以 MS-DOS 日期格式來指定日期。 低序位 **單字** 值以 MS-DOS 時間格式指定時間。 時間值的0值代表午夜。 請參閱＜備註＞一節。

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

檔案的最大建立日期。 如果指定此欄位，則正在檢查的檔案必須具有最等於 MaxDate 的建立日期。 此值必須是非負數。 此欄位的格式為 " **WORD**" 類型的兩個壓縮的16位值。 高序位 **單字** 值會以 MS-DOS 日期格式來指定日期。 低序位 **單字** 值以 MS-DOS 時間格式指定時間。 時間值的0值代表午夜。 請參閱＜備註＞一節。

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>語言
</dt> <dd>

檔案所支援的語言。

</dd> </dl>

## <a name="remarks"></a>備註

此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。

使用 [RegLocator 資料表](reglocator-table.md)、 [IniLocator 資料表](inilocator-table.md)、 [CompLocator 資料表](complocator-table.md)和 [DrLocator 資料表](drlocator-table.md)來搜尋簽章。 此資料表的資料行通常不會當地語系化。 如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。

簽名表通常會遵循 Windows Installer 檔案 [版本控制規則](file-versioning-rules.md)。 除非檔案版本相等，否則不會評估簽章資料表的 [語言] 資料行中指定的語言。 [語言] 資料行可確保檔案為所要求版本的特定語言。 沒有任何方法可忽略 [語言] 資料行。 在 [語言] 資料行中輸入的 Null 值會被視為沒有語言的檔案，而且不符合簽章資料表中出現之語言的檔案簽章。 下列範例會搜尋特定版本的 MSI.DLL。

[DrLocator 資料表](drlocator-table.md)

| 簽名\_ | 父代 | 路徑                  | 深度 |
|-------------|--------|-----------------------|-------|
| MsiDll      | ; | c： \\ windows \\ system32 | 0     |



 

[AppSearch 資料表](appsearch-table.md)



| 屬性 | 簽名\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

簽名表



| 簽名 | FileName | MinVersion    | Odata-maxversion | MinSize | MaxSize | MinDate | MaxDate | 語言 |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | ;     | ;  | ;  | ;  | ;  | 0         |



 

在此情況下，以及在 Windows XP SP1 上， [AppSearch 動作](appsearch-action.md) 會將 MSIDLL 設定為 c： \\ Windows \\ system32 \\msi.dll，因為 MSI.DLL 是中性語言的檔案。 如果 [語言] 資料行的值從0變更為1033，則 AppSearch 動作會找不到相符的 msi.dll，且 MSIDLL 屬性未定義。

您無法使用簽章資料表來單獨查詢語言。 若要搜尋檔案的不同語言版本，每個語言版本的簽章資料表中都必須有不同的專案。 如果 [語言] 欄中提供多種語言，則搜尋是針對支援所有語言的檔案。

MinDate 和 MaxDate 資料行的格式為類型為 **WORD** 的兩個壓縮16位值。

日期 **文字**



| Bits | Content                                             |
|------|-----------------------------------------------------|
| 0–4  | 每月的日 (1-31)                              |
| 5-8  | 月 (1 = 一月、2 = 二月，依此類推)         |
| 9-15 | 從1980算起的年位移 (新增1980以取得實際年份)  |



 

時間 **單字**



| Bits  | Content                     |
|-------|-----------------------------|
| 0–4   | 秒除以2        |
| 5-10  |  (0-59) 分鐘              |
| 11-15 | 24小時制的小時 (0-23)  |



 

計算 MinDate 和 MaxDate 域值的公式如下：

 ( (年 1980) \* 512 + 月 \* 32 + 天 ) \* 65536 + 小時 \* 2048 + 分鐘 \* 32 + 秒/2

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



