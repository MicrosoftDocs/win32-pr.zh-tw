---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型17。
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: 自訂動作類型17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c54d19f99c552b731d88ab62926212539381f40e202a044c31a41fd906a7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947986"
---
# <a name="custom-action-type-17"></a>自訂動作類型17

此自訂動作會呼叫以 C 或 c + + 撰寫的動態連結程式庫 (DLL) 。

## <a name="source"></a>來源

DLL 會在目前的會話期間與應用程式一起安裝。 [CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。 自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，在安裝該檔案之後，以及移除之前，必須呼叫這個自訂動作。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                          | 十六進位 | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  + **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

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

自訂動作會在不同的執行緒中執行，而且可能會對系統有有限的存取權。 以非同步方式執行的自訂動作會在目前序列或安裝會話終止時封鎖主執行緒，直到它們傳回為止。

參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 17 (DLL) ）必須遵守下列排序限制：

-   自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。 這是為了讓自訂動作能夠解析尋找 DLL 所需的路徑。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> <dt>

[延後執行自訂動作](deferred-execution-custom-actions.md)
</dt> <dt>

[動態連結程式庫](dynamic-link-libraries.md)
</dt> </dl>

 

 



