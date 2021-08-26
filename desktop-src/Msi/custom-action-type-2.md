---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型2。
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: 自訂動作類型2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba648578ecdd9d300a5cf15793e3abd9407f78853830f49c16a26db184ff3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996848"
---
# <a name="custom-action-type-2"></a>自訂動作類型2

此自訂動作會呼叫使用命令列啟動的可執行檔。

## <a name="source"></a>來源

可執行檔是從暫時二進位資料流程產生的。 [CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。 二進位資料表中的資料行包含資料流程資料。 針對每個資料列配置個別的資料流程。

您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。 叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                          | 十六進位 | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  + **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標資料行包含來源資料行中所指定之可執行檔的命令列字串。

## <a name="return-processing-options"></a>傳回處理選項

在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 CustomAction 資料表的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。 安裝程式會將任何其他傳回值視為失敗。 若要忽略傳回值，請在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。

## <a name="remarks"></a>備註

啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。 如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。

匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。 如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 格式。 持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> <dt>

[可執行檔](executable-files.md)
</dt> </dl>

 

 
