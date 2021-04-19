---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型34。
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: 自訂動作類型34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997851"
---
# <a name="custom-action-type-34"></a>自訂動作類型34

此自訂動作會呼叫使用命令列啟動的可執行檔。 如需詳細資訊，請參閱 [可執行檔](executable-files.md)。

## <a name="source"></a>來源

可執行檔是從檔案產生的。 [CustomAction](customaction-table.md)資料表的來源欄位包含[目錄](directory-table.md)資料表中的索引鍵。 參考的目錄資料表專案可用來解析工作目錄的完整路徑。 這不一定要是包含可執行檔之目錄的路徑。

## <a name="type-value"></a>類型值

在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                         | 十六進位 | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  + **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>目標

[CustomAction](customaction-table.md)資料表的目標資料行包含可執行檔的完整路徑和名稱，後面加上可執行檔的選擇性引數。 需要可執行檔的完整路徑和名稱。 引號必須用在長的檔案名或路徑周圍。 值會被視為 [格式化](formatted.md) 的文字，而且可能包含屬性、檔案、目錄或其他格式化文字屬性的參考。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction](customaction-table.md) 資料表的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

[可執行檔](executable-files.md)的自訂動作必須傳回0值才能成功。 安裝程式會將任何其他傳回值視為失敗。 若要忽略傳回值，請在 [CustomAction](customaction-table.md)資料表的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。

## <a name="remarks"></a>備註

啟動可執行檔的自訂動作會採用命令列，通常會包含動態指定的屬性。 如果這也是 [延後執行自訂動作](deferred-execution-custom-actions.md)，則安裝程式會在從安裝腳本叫用自訂動作時，使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 或 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 來建立進程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 
