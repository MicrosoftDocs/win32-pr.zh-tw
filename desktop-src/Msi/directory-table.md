---
description: 目錄資料表會指定產品的目錄配置。 資料表的每個資料列都表示來源與目標的目錄。
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: 目錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19e9b5994062ac55564799854fc36016fc6ddb9887bc36aa9a94652ef31aeb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947342"
---
# <a name="directory-table"></a>目錄資料表

目錄資料表會指定產品的目錄配置。 資料表的每個資料列都表示來源與目標的目錄。

目錄資料表具有下列資料行。



| Column            | 類型                         | 答案 | Nullable |
|-------------------|------------------------------|-----|----------|
| 目錄         | [識別碼](identifier.md) | Y   | N        |
| 目錄 \_ 父系 | [識別碼](identifier.md) | N   | Y        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>目錄
</dt> <dd>

目錄資料行包含目錄或目錄路徑的唯一識別碼。 此資料行可以包含屬性的名稱，該屬性會設定為目標目錄的完整路徑。 如果此資料行包含屬性，則目標目錄會使用 DefaultDir 資料行中指定的名稱，並採用目錄父資料行中指定的上層目錄 \_ 。

來原始目錄一律採用 DefaultDir 資料行中指定的名稱，並採用目錄父資料行中指定的上層目錄 \_ 。

如果目錄 \_ 父資料行的值為 null 或等於目錄資料行的值，則目錄資料行代表根目標目錄。 目錄資料表中只能指定一個根目錄。

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>目錄 \_ 父系
</dt> <dd>

此資料行是目錄的上層目錄參考。 具有 \_ 等於 null 或等於目錄資料行之目錄父資料行的記錄，代表根目錄。 父目錄的完整路徑會以傳址方式解析，目錄 \_ 父資料行是目錄資料行中的外部索引鍵。 例如，如果資料夾具有名為 PDIR 的父目錄，則 PDIR 的父目錄會在目錄資料行中具有 PDIR 的資料列的目錄父資料行中提供 \_ 。

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

DefaultDir 資料行包含目錄名稱 (可當地語系化的) 在上層目錄下。 根據預設，這是目標和來原始目錄的名稱。 若要指定不同的來源和目標目錄名稱，請以冒號分隔目標和來源名稱，如下所示： \[ targetname：未通過 \] \[ \] 。

如果目錄父資料行的值 \_ 為 null 或等於目錄資料行，DefaultDir 資料行會指定根來原始目錄的名稱。

針對非根目錄來原始目錄， (. ) 在來原始目錄名稱的 DefaultDir 資料行或目標目錄名稱中輸入，表示目錄應該位於其父目錄中，而不含子目錄。

此資料行中的目錄名稱可能會格式化為簡短的檔案名組 \| 長檔名組。

</dd> </dl>

## <a name="remarks"></a>備註

資料表中的每一筆記錄都代表來源和目的地影像中的目錄。 目錄資料表必須指定目錄資料行值等於 [**TARGETDIR**](targetdir.md) 屬性的單一根目錄。

針對 [系統管理安裝](administrative-installation.md)，請將系統管理映射安裝到名為 TARGETDIR 的根目錄，並使用來原始目錄名稱來解析目標目錄。

請注意，安裝程式會將一些標準 [屬性](properties.md) 設定為系統資料夾路徑。 如需設定為系統資料夾的屬性清單，請參閱 [屬性參考](property-reference.md) 。

目錄解析會在 [CostFinalize 動作](costfinalize-action.md) 期間執行，如下所示：

### <a name="root-destination-directory"></a>根目的地目錄

可能只有一個根目的地目錄。 若要指定根目的地目錄，請將 [目錄] 資料行設定為 [ [**TARGETDIR**](targetdir.md) ] 屬性，並將 [DefaultDir] 資料行設定為 [ [**SourceDir**](sourcedir.md) ] 屬性。 如果定義了 **TARGETDIR** 屬性，則會將目的地目錄解析為屬性的值。 如果未定義 **TARGETDIR** 屬性，則會使用 [**ROOTDRIVE**](rootdrive.md) 屬性來解析路徑。

### <a name="root-source-directory"></a>根來原始目錄

根目錄專案的 DefaultDir 資料行值必須設定為 [**SourceDir**](sourcedir.md) 屬性。

### <a name="non-root-destination-directories"></a>非根目錄目的地目錄

非根目錄的目錄值也會被解釋為定義目的地位置之屬性的名稱。 如果已定義屬性，則會將目的地目錄解析為屬性的值。 如果未定義屬性，則會將目的地目錄解析為目錄父專案的已解析目的地目錄下的子目錄 \_ 。 DefaultDir 值會定義子目錄的名稱。

### <a name="non-root-source-directories"></a>非根目錄來原始目錄

非根目錄的來原始目錄會解析為目錄父專案之已解析來原始目錄的子目錄 \_ 。 同樣地，DefaultDir 值會定義子目錄的名稱。

### <a name="short-or-long-file-names"></a>簡短或長檔名

解析目的地目錄時，如果已設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性，或目錄所在的磁片區不支援長檔名，則會使用 DefaultDir 資料行中指定的簡短檔案名。 否則，會使用完整的檔案名。

請注意，當您在 CostFinalize 動作期間解析目錄時，目錄資料表中的索引鍵會變成將 [屬性](properties.md) 設為目錄路徑。

[CreateFolder 資料表](createfolder-table.md)

若要在安裝期間建立空的資料夾，請參閱 [CreateFolder Table](createfolder-table.md)。

[使用目錄資料表](using-the-directory-table.md)

如需目錄資料表（包括範例）的詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



