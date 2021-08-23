---
description: 如果您在 ICE 參考中所列的現有 ICE 自訂動作之間找不到您需要的內部一致性評估工具，您將需要準備自己的 ICE 來驗證您的套件。
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: 打造冰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4b79ab8e17d53ccfb60484c0d307f668c44a7a0e530cf776b10e73a697541c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500760"
---
# <a name="building-an-ice"></a>打造冰

如果您在[Ice 參考](ice-reference.md)中所列的現有 ICE 自訂動作之間找不到您需要的[內部一致性評估](internal-consistency-evaluators-ices.md)工具，您將需要準備自己的 ice 來驗證您的套件。

撰寫 ICE 自訂動作時，您應該執行下列作業：

-   只以顯示的表格中所列的自訂動作為依據。
-   呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 並張貼 INSTALLMESSAGE \_ 使用者類型的訊息。 撰寫 ICE 訊息時，請遵循 [ICE 訊息指導方針](ice-message-guidelines.md)中的訊息格式。
-   撰寫您的 ICE，讓它能捕捉任何 API 錯誤，而且一律會傳回錯誤 \_ 成功。 這是必要的，以允許後續自訂動作在 ICE 失敗後執行。

ICE 自訂動作僅限於下列自訂動作類型。



| 自訂動作類型                                 | 描述               |
|----------------------------------------------------|---------------------------|
| [自訂動作類型1](custom-action-type-1.md)   | 二進位資料流程中的 DLL      |
| [自訂動作類型2](custom-action-type-2.md)   | 二進位資料流程中的 EXE      |
| [自訂動作類型5](custom-action-type-5.md)   | 二進位資料流程中的 JScript  |
| [自訂動作類型6](custom-action-type-6.md)   | 二進位資料流程中的 VBScript |
| [自訂動作類型37](custom-action-type-37.md) | 以字串形式 JScript 程式碼    |
| [自訂動作類型38](custom-action-type-38.md) | VBScript 程式碼字串   |



 

撰寫 ICE 自訂動作時，請勿執行下列動作：

-   請勿假設 ICE 所接收引擎的控制碼是安裝程式資料庫的安裝實例。 如果不是安裝實例，就不會定義某些屬性、不會解析來源和目標目錄，也不會定義目前的功能狀態。
-   請勿依賴任何安裝程式動作、自訂動作或其他 ICE 的先前執行或非執行。 因為先前的 ICE 可能已在任何資料表中建立暫存資料行，所以作者應該盡可能依名稱參考資料行。 在結束之前，請先清除任何暫時的資料行或資料表。
-   請勿假設作者可以存取資料庫來原始目錄的影像。
-   請勿假設對資料庫所做的變更不會保存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[C + + 中的範例 ICE](sample-ice-in-c-.md)
</dt> <dt>

[VBScript 中的範例 ICE](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



