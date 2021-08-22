---
description: 若要協助維護軟體安裝的安全，請在撰寫 Windows Installer 自訂動作時遵守這些指導方針。
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: 保護自訂動作的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b5ea12bd8d38025587cb09fd7a17d3e87739acedf31d85f72ff4b1b76b0432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649288"
---
# <a name="guidelines-for-securing-custom-actions"></a>保護自訂動作的指導方針

在使用自訂動作撰寫 Windows Installer 套件時遵循下列指導方針，可協助您在安裝期間維護安全的環境：

-   保護您自訂動作所撰寫的任何其他檔案。
-   檢查緩衝區長度和自訂動作讀取的所有資料的有效性。 這包括可提供資料給您自訂動作的屬性，特別是使用使用者所提供之公用屬性的屬性。
-   請勿依賴您的安裝套件要執行之所有平臺上的系統不信任的外部 Dll。
-   請仔細考慮是否要使用使用較 [*高*](e-gly.md) 許可權或模擬的自訂動作。 自訂動作（例如「在安裝完成後開啟 URL」、「安裝完成後啟動軟體」或「在安裝完成後啟動讀我檔案」）通常不需要更高的許可權才能運作。 如果您的自訂動作必須以較 *高* 的許可權執行，請確定自訂動作程式碼可預防緩衝區溢位，並不慎載入 unsafe 程式碼。 請注意，在安裝的執行時間期間，安裝程式會將資訊以較 *高* 的許可權傳遞給處理常式，並執行腳本。 在執行階段期間執行的任何自訂動作，都可能以較 *高* 的許可權執行。
-   收集使用者在 UI 順序期間提供的所有資訊。 請勿提示使用者提供任何無法使用公用屬性設定的資訊。
-   如果您的腳本自訂動作會展開屬性，請預防自訂動作受到保護，以避免腳本插入的可能性。 腳本可能會以純文字的方式登入。

另請參閱 [自訂動作安全性](custom-action-security.md)。

 

 



