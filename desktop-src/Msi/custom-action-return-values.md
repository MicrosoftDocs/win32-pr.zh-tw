---
description: 如果未設定 msidbCustomActionTypeContinue 傳回處理選項，自訂動作必須傳回整數狀態碼，如下表所示。
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: 自訂動作傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3853cfeafba22cb2d479feb1e699c29bcf4b0ab7a08402245f30958cb593df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044998"
---
# <a name="custom-action-return-values"></a>自訂動作傳回值

如果未設定 **msidbCustomActionTypeContinue** 傳回處理選項，自訂動作必須傳回整數狀態碼，如下表所示。



| 傳回值                 | 描述                           |
|------------------------------|---------------------------------------|
| \_ \_ 未 \_ 呼叫錯誤函式 | 未執行動作。                  |
| 錯誤 \_ 成功               | 已成功完成動作。       |
| \_安裝 \_ USEREXIT 時發生錯誤     | 使用者提前終止。          |
| \_安裝 \_ 失敗時發生錯誤      | 發生無法復原的錯誤。         |
| \_沒有 \_ 其他 \_ 專案的錯誤       | 略過其餘的動作，而不是錯誤。 |



 

請注意， [可執行檔](executable-files.md) 的自訂動作必須傳回0值才能成功。 安裝程式會將任何其他傳回值視為失敗。 若要忽略傳回值，請在 [CustomAction 資料表](customaction-table.md)的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。

如需有關 **msidbCustomActionTypeContinue** 選項和其他傳回處理選項的詳細資訊，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。 例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。 如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤碼](error-codes.md)
</dt> <dt>

[動作傳回值的記錄](logging-of-action-return-values.md)
</dt> </dl>

 

 



