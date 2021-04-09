---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型18。
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: 自訂動作類型18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945208"
---
# <a name="custom-action-type-18"></a>自訂動作類型18

此自訂動作會呼叫使用命令列啟動的可執行檔。

## <a name="source"></a>來源

可執行檔是從隨應用程式安裝的檔案產生的。 [CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。 自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，必須在安裝檔案之後以及移除之前呼叫這個自訂動作。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                          | 十六進位 | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  + **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標資料行包含在來源資料行中所識別之可執行檔的命令列字串。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。 安裝程式會將任何其他傳回值視為失敗。 若要忽略傳回值，請在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。

## <a name="remarks"></a>備註

啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。 如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。

參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 18 (EXE) ）必須遵守下列排序限制：

-   自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。 這是為了讓自訂動作能夠解析尋找 EXE 所需的路徑。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> <dt>

[可執行檔](executable-files.md)
</dt> </dl>

 

 
