---
description: CompLocator 資料表包含尋找使用安裝程式設定資料之檔案或目錄所需的資訊。
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: CompLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514153"
---
# <a name="complocator-table"></a>CompLocator 資料表

CompLocator 資料表包含尋找使用安裝程式設定資料之檔案或目錄所需的資訊。

CompLocator 資料表包含下列資訊。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |
| ComponentId | [GUID](guid.md)             | N   | N        |
| 類型        | [整數](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>資料行資訊

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

此資料行代表唯一的檔案簽章，而且也是簽章 [資料表](signature-table.md)中的外部金鑰。 如果簽章資料表中的索引鍵不存在，則會假設搜尋是為了讓 CompLocator 資料表所指向的目錄存在。

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

元件的元件識別碼，其金鑰路徑會用於搜尋。 這應該是元件 [資料表](component-table.md)的 [元件] 欄位中所顯示元件的 GUID。 它可能是屬於電腦上所安裝之另一個產品之元件的元件識別碼。 它不應該是出現在 [PublishComponent 資料表](publishcomponent-table.md)之 [元件] 欄位中的已發行元件的 GUID。

若要尋找另一個產品所安裝之檔案的元件識別碼 GUID 值，請移至產品的安裝套件。 移至 [檔案] [資料表](file-table.md) ，並尋找包含檔案之檔案識別碼的資料列。 此資料列的 [元件] 資料 \_ 行包含控制檔案之元件的元件識別碼。 移至 [元件資料表](component-table.md) ，並在 [元件] 資料行中尋找包含此元件識別碼的資料列。 此資料列的 [元件識別碼] 資料行包含元件識別碼 GUID。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

布林值，判斷元件的金鑰路徑是否為檔案名或目錄位置。

下表列出有效的值。 如果不存在，則類型會設定為1， (一個) 。



| 常數                      | 十六進位 | Decimal | Description              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | 金鑰路徑是目錄。 |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | 金鑰路徑是檔案名。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。

一般而言，此資料表中的資料行並不會當地語系化。 如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。

如需詳細資訊，請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



