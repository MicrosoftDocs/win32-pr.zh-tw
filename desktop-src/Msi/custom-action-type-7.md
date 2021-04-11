---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型7。
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: 自訂動作類型7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026885"
---
# <a name="custom-action-type-7"></a>自訂動作類型7

自訂動作類型7會搭配並行安裝使用。 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。

此自訂動作會安裝另一個內嵌于第一個封裝內的安裝程式套件。

## <a name="source"></a>來源

並行應用程式的資料庫會儲存為封裝的 substorage，而 substorage 的名稱則是在 [CustomAction 資料表](customaction-table.md)的 [來源] 欄位中指定。

## <a name="numeric-type"></a>數字類型



| 類型名稱                                                      | 值 |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標欄位包含要傳遞至並行安裝的屬性設定。 這些屬性設定可以指定功能。

## <a name="return-processing-options"></a>傳回處理選項

並行安裝會話會以另一個執行緒的形式在目前的進程中執行。 並行安裝無法以非同步方式執行。

請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

選項旗標可用來控制自訂動作的潛在多次執行。 請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

此自訂動作不會使用此選項。

## <a name="return-values"></a>傳回值

從並行安裝的使用者結束、失敗、暫停或成功傳回狀態的處理方式，與其他任何動作的處理方式相同。 不過請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。 例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。 如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。

請注意，如果同時安裝同時安裝了 **msidbCustomActionTypeContinue** ，則會傳回錯誤 \_ 安裝 \_ USEREXIT、錯誤 \_ 安裝 \_ 重新開機、錯誤安裝重新開機， \_ \_ \_ 或 \_ 需要錯誤成功 \_ 重新開機， \_ 以視為錯誤 \_ 成功。 這表示，如果您設定 **msidbCustomActionTypeContinue** ，且您的並行安裝需要重新開機，則會忽略重新開機的需求。 此外，也會忽略來自並行安裝自訂動作的錯誤碼。

如果未設定 **msidbCustomActionTypeContinue** ，則會將下列傳回碼和錯誤 \_ 成功視為成功，並具有下列意義。 其他傳回碼會視為失敗。



| 訊息                          | 意義                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| \_安裝 \_ 重新開機時發生錯誤           | 重新開機旗標將會設定為在安裝結束時重新開機。                                  |
| \_安裝 \_ 立即重新開機 \_ 時發生錯誤      | 需要重新開機，才能完成安裝。 重新開機將會立即處理。 |
| \_ \_ 需要重新開機 \_ 錯誤 | 需要重新開機，但已隱藏。                                                          |



 

## <a name="remarks"></a>備註

在安裝或移除相關聯的元件或功能時，必須要有條件運算式才能啟用並行安裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[並行安裝](concurrent-installations.md)
</dt> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> <dt>

[關於自訂動作](about-custom-actions.md)
</dt> <dt>

[使用自訂動作](using-custom-actions.md)
</dt> <dt>

[自訂動作傳回值](custom-action-return-values.md)
</dt> </dl>

 

 



