---
description: 您可以使用此資料表來撰寫多套件安裝。
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: MsiEmbeddedChainer 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfcf48f3cf3863f19819b3337a136d2540fa3254067cacc50fcf391256caa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945053"
---
# <a name="msiembeddedchainer-table"></a>MsiEmbeddedChainer 資料表

您可以使用此資料表來撰寫 [多套件安裝](multiple-package-installations.md)。 MsiEmbeddedChainer 資料表中的每個資料列都會參考不同的使用者定義函數，可用來從單一封裝安裝多個 Windows Installer 套件。 使用者定義函數的[可執行檔](executable-files.md)會儲存在 Windows Installer 套件內。

**[Windows Installer 4.0 或更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此資料表。

**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md)角色的 Windows Server 2008 R2：** 不支援。 如果啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色，使用 MsiEmbeddedChainer 資料表的多個套件安裝將會失敗。

若要從單一封裝安裝多個封裝，MsiEmbeddedChainer 資料表中所列的其中一個使用者定義函數必須在評估為執行動作的條件欄位中具有條件陳述式。 如果有一個以上的函式具有評估為執行的條件，則只能執行一個函數。 這種情況是錯誤，無法保證將會執行哪些函數。 如果安裝需要其他自訂動作，則應該在 [CustomAction 資料表](customaction-table.md) 和順序資料表中撰寫這些動作。

這些函式必須藉由呼叫 [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) 函式來加入目前的安裝，而且必須呼叫 [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) 函數來認可多個封裝的安裝。 如果函式在呼叫 **MsiEndTransaction** 之前傳回，安裝程式會復原所有安裝。

MsiEmbeddedChainer 資料表具有下列資料行。



| Column             | 類型                             | 答案 | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [識別碼](identifier.md)     | Y   | N        |
| 條件          | [Condition](condition.md)       | N   | Y        |
| CommandLine        | [格式 化](formatted.md)       | N   | Y        |
| 來源             | [CustomSource](customsource.md) | N   | N        |
| 類型               | [整數](integer.md)           | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

資料表的主要索引鍵。 這個值是這個資料列所描述的使用者定義函數的唯一識別碼。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

執行使用者定義函數的條件陳述式。 您可以啟用或停用 MsiEmbeddedChainer 資料表中所列的函式，並使用會修改此欄位所評估之屬性值的轉換。 如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>命令
</dt> <dd>

此欄位中的值是傳遞至來源資料行中所識別之可執行檔的命令列字串的一部分。 安裝程式會將此欄位中的值附加至交易控制碼，以產生命令列。 如果此資料行中的值為 null，則命令列只會包含交易控制碼。

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源
</dt> <dd>

使用者定義函數之可執行檔的位置。 如果 [類型] 資料行中的值是2，這個資料行就可以將外部索引鍵包含在 [二進位資料表](binary-table.md)中。 如果 Type 資料行中的值為18，則這個資料行可以在檔案 [資料表](file-table.md)中包含外部索引鍵。 如果 Type 資料行中的值為50，則這個資料行可以在 [屬性工作表](property-table.md)中包含外部索引鍵。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

MsiEmbeddedChainer 資料表中所列的函式會使用下列自訂動作數數值型別來描述。 此資料行只能包含下列三個數數值型別的值：自訂動作旗標的任何其他組合都會被忽略。



| 自訂動作類型                                 | 自訂動作旗標                                                | 十六進位 | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [自訂動作類型2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  + **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [自訂動作類型18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  + **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [自訂動作類型50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  + **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>備註

Windows Installer 不會防止此資料表中的使用者定義函式在應用程式的公告期間執行。 您可以在 [條件] 資料行中使用條件陳述式，以防止函數在公告期間執行。

Windows Installer 也提供非內嵌的外部 UI 處理常式，可在 Windows Installer 封裝之上建立豐富的使用者介面。 如需有關使用外部 UI 處理常式搭配 Windows Installer 的詳細資訊，請參閱[使用 MsiSetExternalUI 監視安裝](monitoring-an-installation-using-msisetexternalui.md)。

[MsiPackageCertificate 資料表](msipackagecertificate-table.md)會列出數位簽章憑證，用來驗證進行多套件安裝之安裝套件的身分識別。 您可以使用此表格來減少多套件安裝在需要系統管理員回應的 (UAC) 提示字元中，顯示 [*使用者帳戶控制*](u-gly.md) 的次數。

 

 
