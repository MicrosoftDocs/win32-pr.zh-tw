---
description: 內部一致性評估工具（也稱為「Ices-003」）是以 VBScript、JScript 或 DLL 或 EXE 撰寫的自訂動作。
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: 內部一致性評估工具-Ices-003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988430"
---
# <a name="internal-consistency-evaluators---ices"></a>內部一致性評估工具-Ices-003

內部一致性評估工具（也稱為「Ices-003」）是以 VBScript、JScript 或 DLL 或 EXE 撰寫的自訂動作。 當執行這些自訂動作時，它們會在資料庫記錄中，針對在個別檢查時有效的專案，掃描資料庫中的專案，但這可能會在整個資料庫的內容中造成不正確的行為。 請注意，這與使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)對個別記錄進行的驗證不同。

例如， [元件資料表](component-table.md) 可能會列出數個在使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)個別測試時都有效的元件。 不過，當兩個元件使用相同的 [GUID](guid.md)做為其元件程式碼時， **MsiViewModify** 不會攔截錯誤。 自訂動作 [ICE08](ice08.md) 的設計目的是要驗證元件資料表不包含重複的元件程式碼 guid。

ICE 自訂動作會傳回四種訊息：

-   [**錯誤**](merge-errors.md) 錯誤訊息報表資料庫撰寫會導致不正確的行為。 例如，重複的元件 Guid 會導致安裝程式不正確地註冊元件。
-   **警告** 在特定情況下，會導致不正確行為的警告訊息報告資料庫撰寫。 警告也可以報告資料庫撰寫的非預期副作用。 例如，在兩個條件中輸入相同的屬性名稱，這兩個條件只會與名稱中的字母大小寫不同。 因為安裝程式會區分大小寫，所以安裝程式會將這些視為不同的屬性。
-   **失敗** 失敗訊息會回報 ICE 自訂動作失敗。 失敗的原因通常是因為 ICE 根本無法執行的資料庫發生這類嚴重問題。
-   **參考資訊** 參考用訊息提供 ICE 的資訊，而且不表示資料庫有問題。 它們通常是 ICE 本身的相關資訊，例如簡短的描述。 它們也可以在 ICE 執行時提供進度資訊。

如需詳細資訊，請參閱 [使用內部一致性評估](using-internal-consistency-evaluators.md)工具。

 

 



