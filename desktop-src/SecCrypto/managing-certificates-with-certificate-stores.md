---
description: 使用 CryptoAPI 函式來管理憑證存放區和這些存放區中的憑證、憑證撤銷清單，以及憑證信任清單。
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: 使用憑證存放區管理憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0bfab57522ea8b400ee8d042b5b2cb1ad37fe7c234a291000eb516b11a6be0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425650"
---
# <a name="managing-certificates-with-certificate-stores"></a>使用憑證存放區管理憑證

經過一段時間後， [*憑證*](../secgloss/c-gly.md) 就會累積在使用者的電腦上。 需要工具才能管理這些憑證。 [*CryptoAPI*](../secgloss/c-gly.md) 提供這些工具作為函式來儲存、取出、刪除、列出 (列舉) ，以及驗證憑證。 CryptoAPI 也提供將憑證附加至訊息的方法。

CryptoAPI 提供兩種主要的函式類別來管理憑證：管理 [*憑證存放區*](../secgloss/c-gly.md)的函式、用來處理憑證的函式、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) ，以及在這些存放區內 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。

管理 [*憑證存放區*](../secgloss/c-gly.md) 的函式包含使用邏輯或 [*虛擬存放區*](../secgloss/v-gly.md)、 [*遠端存放*](../secgloss/r-gly.md)區、 [*外部*](../secgloss/e-gly.md)存放區，以及可重新放置之存放區的功能。

憑證、 [*crl*](../secgloss/c-gly.md)和 [*ctl*](../secgloss/c-gly.md) 可以保留並保留在 [*憑證存放區*](../secgloss/c-gly.md)中。 您可以從存放區的存放區中取出它們，以便在驗證程式中使用它們。

[*憑證存放區*](../secgloss/c-gly.md)是所有憑證功能的核心。 憑證會在存放區中使用具有 "Cert" 前置詞的函式進行管理。 一般憑證存放區是連結的 [*憑證*](../secgloss/c-gly.md) 清單，如下圖所示。

![憑證存放區](images/certstore1.png)

上圖顯示：

-   每個 [*憑證存放區*](../secgloss/c-gly.md) 都有指向該存放區中第一個憑證區塊的指標。
-   憑證區塊包含該憑證資料的指標，以及存放區中下一個憑證區塊的「下一步」指標。
-   最後一個憑證區塊中的「下一個」指標會設定為 **Null**。
-   憑證的資料區塊包含唯讀憑證內容和憑證的任何擴充屬性。
-   每個憑證的資料區塊都包含 [*參考計數*](../secgloss/r-gly.md) ，可追蹤存在之憑證的指標數目。

[*憑證存放區*](../secgloss/c-gly.md)中的憑證通常會保留在某種永久儲存區中，例如磁片檔案或系統登錄。 憑證存放區也可以完全在記憶體中建立和開啟。 記憶體存放區提供暫時的憑證儲存體，可處理不需要保留的憑證。

其他存放區位置可讓存放區在本機電腦的登錄區中，或在遠端電腦的登錄中，以適當的許可權設定來保留及搜尋。

每位使用者都有個人的存放區，其中儲存了該使用者的憑證。 「我的存放區」可以是許多實體位置的任意一個，包括本機或遠端電腦上的登錄、磁片檔案、資料庫、目錄服務、 [*智慧卡*](../secgloss/s-gly.md)或其他位置。 雖然任何憑證都可以儲存在「我的存放區」中，但此存放區應保留給使用者的個人憑證：這些憑證用來簽署和解密該使用者的訊息。

使用憑證進行驗證取決於擁有一些受信任的憑證簽發者所發行的憑證。 受信任的憑證簽發者的憑證通常會保留在根存放區中，且目前會保存到登錄子機碼中。 在 CryptoAPI 內容中，根存放區會受到保護，而使用者介面對話方塊會提醒使用者只將受信任的憑證放到該存放區中。 在商業網路的情況下，系統管理員可能會將憑證推送 (從網域控制站電腦) 複製到用戶端電腦上的根存放區。 此程式會提供具有類似信任清單之網域的所有成員。

其他憑證可以存放在 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 系統存放區或使用者建立的檔案型存放區中。

如需使用和維護憑證存放區的函式清單，請參閱 [憑證存放區功能](cryptography-functions.md)。

如需使用其中一些函數的範例，請參閱 [範例 C 程式：憑證存放區作業](example-c-program-certificate-store-operations.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理憑證存放區狀態](managing-a-certificate-store-state.md)
</dt> <dt>

[使用憑證存放區中的憑證](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[憑證連結](certificate-links.md)
</dt> <dt>

[集合存放區](collection-stores.md)
</dt> <dt>

[邏輯與實體存放區](logical-and-physical-stores.md)
</dt> <dt>

[系統存放區位置](system-store-locations.md)
</dt> <dt>

[憑證存放區遷移](certificate-store-migration.md)
</dt> </dl>

 

 
