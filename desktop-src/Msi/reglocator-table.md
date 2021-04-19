---
description: RegLocator 資料表會保存使用登錄搜尋檔案或目錄所需的資訊，或是搜尋特定的登錄專案本身。 此資料表包含下列資料行。
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: RegLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988776"
---
# <a name="reglocator-table"></a>RegLocator 資料表

RegLocator 資料表會保存使用登錄搜尋檔案或目錄所需的資訊，或是搜尋特定的登錄專案本身。 此資料表包含下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |
| Root        | [整數](integer.md)       | N   | N        |
| 答案         | [RegPath](regpath.md)       | N   | N        |
| Name        | [格式 化](formatted.md)   | N   | Y        |
| 類型        | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

[簽章] 欄位中的值 \_ 代表唯一簽章，這是簽章資料表 [的資料](signature-table.md) 行之一的外部索引鍵。 如果簽章資料表中有這個簽章，則會搜尋檔案。 如果簽章資料表中沒有這個簽章，而且 [類型] 資料行的值是 **msidbLocatorTypeRawValue**，則搜尋是針對 RegLocator 資料表所指向的登錄機碼名稱。 否則搜尋是針對 RegLocator 資料表所指向的目錄。

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>根
</dt> <dd>

登錄值的預先定義根金鑰。



| 常數                          | 十六進位 | Decimal | 根金鑰             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | HKEY \_ 類別 \_ 根目錄  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | HKEY \_ 目前的 \_ 使用者  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | HKEY \_ 本機 \_ 電腦 |
| **msidbRegistryRootUsers**        | 0x003       | 3       | HKEY \_ 使用者          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

登錄值的索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

登錄值名稱。 如果這個值為 null，則會抓取索引鍵未命名或預設值（如果有的話）的值。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

判斷登錄值是否為檔案名、目錄位置或原始登錄值的值。

下表列出有效的值。 如有必要，請設定前三個值的其中一個，並 **msidbLocatorType64bit** 。 如果此欄位中的專案不存在，則類型會設定為1。



| 常數                      | 十六進位 | Decimal | Description                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | 金鑰路徑是目錄。                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | 金鑰路徑是檔案名。                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | 金鑰路徑是登錄值。                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | 設定此位，讓安裝程式搜尋登錄的64位部分。 請勿將此位設定為讓安裝程式搜尋登錄的32位部分。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

請注意，如果 [類型] 欄位中的值是 **msidbLocatorTypeRawValue**，安裝程式會將 [AppSearch](appsearch-table.md) 資料表的屬性欄位中指定的屬性值設定為登錄值。 安裝程式會將前置詞新增至登錄值，以識別登錄值的型別。 如需登錄數值型別的詳細資訊，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。



| 登錄類型   | 安裝程式新增的前置詞                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ SZ         | 無，但是如果登錄值的第一個字元是 \# ，則安裝程式會在前面加上一個字元來將該字元轉義 \# 。            |
| DWORD           | " \# " （選擇性），後面接著 ' + ' 或 '-'                                                                                                  |
| REG \_ EXPAND \_ SZ | "\#%"                                                                                                                                   |
| REG \_ 多重 \_ SZ  | Null。 安裝程式會將屬性設定為開頭為 null 的值，並以 null 結尾。                                          |
| REG \_ 二進位檔     | " \# x" 如果是 REG \_ 二進位，則安裝程式會將每個十六進位數位轉換成 (半個十六進位數位，並將其儲存為前面加上 "x" 的 ASCII 字元) \# 。 |



 

一般而言，此資料表中的資料行並不會當地語系化。 如果作者決定要搜尋多種語言的產品，則每種語言的表格中都必須包含個別的專案。

請注意，您不能使用 RegLocator 資料表來檢查索引鍵是否存在。 不過，您可以搜尋索引鍵的預設值，如果不是空的，則會取出其值。

如需詳細資訊，請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
