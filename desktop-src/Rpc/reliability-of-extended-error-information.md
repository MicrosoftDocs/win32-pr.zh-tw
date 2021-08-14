---
title: 擴充錯誤資訊的可靠性
description: 延伸的錯誤資訊不可靠。
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cb85e31f993719e5f0a555a63dd83a80064ed76df1ebda43cf03f994dab9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926836"
---
# <a name="reliability-of-extended-error-information"></a>擴充錯誤資訊的可靠性

延伸的錯誤資訊不可靠。 擴充的錯誤資訊無法用於建立程式碼邏輯。 您可以檢查是否有延伸的錯誤資訊，如果有的話，要傾印、儲存或記錄這些資訊。 但請勿依賴資訊或其內容。

下列原因說明擴充錯誤資訊不可靠的原因：

-   擴充錯誤記錄的順序和內容取決於系統的內部架構，而這些架構可能會變更。 某些作業可能會在目前的系統上 NPFS，但未來可能會通過 TCP。 這些不同的元件會產生非常不同的錯誤碼，因此程式碼檢查原本就不可靠，因此不建議使用。
-   如先前所述，您可以停用擴充錯誤資訊的傳播。 如果包含偵測程式碼，應用程式可能會在特定環境中停止運作。
-   擴充錯誤資訊的傳播會以最大的方式執行。 如果電腦上沒有足夠的記憶體可處理或傳播鏈，則傳播或產生擴充的錯誤資訊可能會失敗。 在這種情況下，將會捨棄鏈。 某些通訊協定的錯誤長度有限，因為它們通常不包含許多資訊。 如果鏈的長度超過允許的封包長度，RPC 執行時間就會開始從鏈中卸載資訊，以嘗試將鏈放入封包中。 執行時間會先卸載倒數第二記錄開始的記錄，直到只剩下第一個和最後一個記錄為止。 如果鏈仍無法放入封包中，則執行時間會卸載字串參數和電腦名稱稱。 如果已卸載字串參數，參數的類型會設為 none。 如果記錄已卸載，則會在下一筆記錄中設定 EEInfoNextRecordsMissing 旗標，並在上一筆記錄中設定 EEInfoPreviousRecordsMissing。

 

 




