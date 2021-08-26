---
description: 下列各節中的範例程式會執行需要公開/私密金鑰組才能加密和解密檔案、訊息和簽章的作業。
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: 必要的金鑰容器、金鑰和憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee5f86f887050d0d7abe440c89cc9c9444dba26854645d5ad6d16279af91e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992718"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>必要的金鑰容器、金鑰和憑證

下列各節中的範例程式會執行需要 [*公開/私密金鑰*](../secgloss/p-gly.md) 組才能加密和解密檔案、訊息和簽章的作業。 其中有許多程式會在執行時間進行編譯、連結及執行，但不會有適當的 [*金鑰容器*](../secgloss/k-gly.md)、金鑰、 [*憑證存放區*](../secgloss/c-gly.md)和憑證存在於這些存放區中。

此外，「我的存放區」中的某些憑證必須設定部分的擴充屬性。

若要建立所需的預設金鑰容器，您可以執行 [C 程式範例中的程式：建立金鑰容器和產生金鑰](example-c-program-creating-a-key-container-and-generating-keys.md)。 請注意，金鑰容器的建立不會自動產生公開/私密金鑰組。 但是，範例程式會建立金鑰容器，並產生公開/私密金鑰組。

在產生公開/私密金鑰組之後，您可以從 [*憑證授權單位*](../secgloss/c-gly.md) 單位)  (CA 取得測試憑證（使用這些金鑰）。

有幾個程式假設具有特定主體名稱的憑證存在於 [我的系統] 存放區中。 尤其是，有數個程式會尋找主體名稱為 "Full Test Cert" 和 "Hortense" 的憑證。 您可以在程式碼中變更憑證的主體名稱，以符合「我的憑證存放區」中存在之憑證的主體名稱。

在 [範例 C 程式中執行範例程式：列出存放區](example-c-program-listing-the-certificates-in-a-store.md) 中的憑證將會顯示存放區中的所有憑證，以及在這些憑證上設定的所有擴充屬性。

 

 
