---
description: 錯誤隔離和 Failfast 原則
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: 錯誤隔離和 Failfast 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510519"
---
# <a name="fault-isolation-and-failfast-policy"></a>錯誤隔離和 Failfast 原則

COM + 會執行廣泛的內部完整性和一致性檢查。 如果 COM + 遇到未預期的內部錯誤狀況，則會立即終止進程。 這個稱為 *failfast* 的原則可加速錯誤內含專案，並產生更可靠且健全的系統。

請考慮 COM + 偵測到其中一個資料結構處於損毀狀態的情況。 此時，原因和損毀的程度都不明，但不幸的是，COM + 無法分辨損毀的分散程度。 不過，雖然 COM + 處於不定狀態，但它並不會在隔離的情況下執行。 就像其他 Dll 一樣，它是裝載在進程環境中，並與主要程式可執行檔和許多其他 Dll 共用單一位址空間。 因此，COM + 會假設整個程式已損毀，而且程式會立即終止，以防止它將可能損毀的資訊散佈到其他進程，或更糟的是，不允許認可損毀的資料並使其成為持久的。

COM + 不允許在內容外傳播例外狀況。 如果在 COM + 內容中執行時發生例外狀況，而且應用程式在從內容傳回之前未攔截到例外狀況，COM + 會攔截例外狀況並結束進程。 在此情況下，使用 failfast 原則是以例外狀況將進程置於不定狀態的假設為基礎。繼續處理並不安全。

如果您是開發人員或系統管理員，您應該檢查事件檢視器的應用程式記錄檔，以取得任何 failfast 動作或嚴重應用程式錯誤的詳細資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[找出錯誤的來源](finding-the-source-of-an-error.md)
</dt> <dt>

[COM + 如何修改傳回值](how-com--modifies-return-values.md)
</dt> <dt>

[解讀錯誤碼](interpreting-error-codes.md)
</dt> <dt>

[在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[疑難排解](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



