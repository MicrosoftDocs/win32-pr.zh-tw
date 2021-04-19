---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型6。
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: 自訂動作類型6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994375"
---
# <a name="custom-action-type-6"></a>自訂動作類型6

此自訂動作是以 VBScript 撰寫的。 如需詳細資訊，請參閱 [腳本](scripts.md)。

## <a name="source"></a>來源

腳本是從暫時性二進位資料流程產生的。 [CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。 二進位資料表中的資料行包含資料流程資料。 針對每個資料列配置個別的資料流程。

您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。 叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。



| 常數                                                               | 十六進位 | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeBinaryData** | 0x006       | 6       |



 

Windows Installer 可以在64位作業系統上使用64位自訂動作。 以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。 如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。 在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。



| 常數                                                                                                      | 十六進位 | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeBinaryData**  + **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。 處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

以腳本撰寫的選擇性函式必須傳回 [JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。

## <a name="remarks"></a>備註

以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話物件**](session-object.md)。 安裝程式會使用名稱 *會話* 將 **會話** 物件附加至腳本。 因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。

匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。 如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 檔案名格式。 持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 



