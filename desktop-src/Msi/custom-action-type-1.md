---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型1。
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: 自訂動作類型1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3437fcd8a9a0da84ecb03f2527d30b6644210b2feb2ccc6c5f6558c3667a0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044898"
---
# <a name="custom-action-type-1"></a>自訂動作類型1

此自訂動作會呼叫以 C 或 c + + 撰寫的動態連結程式庫 (DLL) 。

## <a name="source"></a>來源

DLL 是從暫存二進位資料流程產生的。 [CustomAction 資料表](customaction-table.md)的來源欄位包含[二進位資料表](binary-table.md)的索引鍵。

二進位資料表中的資料行包含資料流程資料。 針對每個資料列配置個別的資料流程。 您可以使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ，然後使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入資料表中，以從檔案插入新的二進位資料。 叫用自訂動作時，資料流程資料會複製到暫存檔，然後根據自訂動作的類型進行處理。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的類型資料行中包含下列旗標位，以指定基本的數數值型別。



| 常數                                                          | 十六進位 | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  + **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

## <a name="target"></a>目標

DLL 是透過 [CustomAction 資料表](customaction-table.md)的目標欄位中名為的進入點來呼叫，並傳遞做為目前安裝會話控制碼的單一引數。 資料表中指定的進入點名稱必須符合從 DLL 匯出的專案點名稱。 請注意，如果未指定專案函數，則為。DEF 檔案或/EXPORT：連結器規格，名稱可能會有前置底線和 " @4 " 尾碼。 呼叫的函式必須指定 \_ \_ stdcall 呼叫慣例。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

請參閱 [自訂動作傳回值](custom-action-return-values.md)。

## <a name="remarks"></a>備註

呼叫動態連結程式庫 (DLL) 的自訂動作需要安裝會話的控制碼。 如果這也是延後執行自訂動作，則在執行安裝腳本時，會話可能不再存在。 如需此類型的自訂動作如何取得內容資訊的相關資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。

匯出資料庫資料表時，會將每個資料流程寫入至資料表所命名之子資料夾中的個別檔案，並使用主鍵作為二進位資料表) 的檔案名 (名稱資料行，且預設副檔名為 "ibd"。 如果檔案系統或版本控制系統不支援長檔名，則名稱應該使用8.3 格式。 持續性封存檔案會以使用的檔案名取代資料流程資料，讓您可以在匯入資料表時找出資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> <dt>

[動態連結程式庫](dynamic-link-libraries.md)
</dt> <dt>

[取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



