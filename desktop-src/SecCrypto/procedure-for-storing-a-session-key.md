---
description: 說明用於儲存工作階段金鑰的程式。
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: 儲存工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977347"
---
# <a name="storing-a-session-key"></a>儲存工作階段金鑰

> [!Note]  
> 本節假設使用者擁有一組 [*公開/私密金鑰*](../secgloss/p-gly.md)組。 如需建立金鑰組的指示和範例，請參閱 [範例 C 程式：建立金鑰容器和產生金鑰](example-c-program-creating-a-key-container-and-generating-keys.md)。

 

**若要儲存工作階段金鑰**

1.  使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函數建立簡單的 [*金鑰 BLOB*](../secgloss/k-gly.md) 。 這會將工作階段金鑰從 CSP 傳送至應用程式的記憶體空間。 指定用來簽署金鑰 BLOB 的交換公開金鑰。
2.  將簽署的金鑰 BLOB 儲存至磁片。 假設所有磁片都不是安全的。
3.  需要金鑰時，請從磁片讀取金鑰 BLOB。
4.  使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式，將金鑰 BLOB 匯入回 CSP。

如需建立 [*工作階段金鑰*](../secgloss/s-gly.md) ，並將該金鑰匯出至可寫入磁片檔案之 [*簡單金鑰 BLOB*](../secgloss/s-gly.md) 的範例，請參閱 [範例 C 程式：匯出工作階段金鑰](example-c-program-exporting-a-session-key.md)。

此程式只提供基本的安全性。 如果預存工作階段金鑰稍後將用來加密資料，則先前的程式並不會提供足夠的安全性。

若要提供更高的安全性，請使用 exchange 私密金鑰簽署金鑰 BLOB，然後再將其儲存至磁片。 當金鑰 BLOB 稍後從磁片讀取時，就可以驗證其簽章，以確保金鑰 BLOB 保持不變。

如果金鑰 BLOB 未簽署，可以存取磁片或儲存金鑰之其他媒體的任何人，都可以建立新的工作階段金鑰。

您可以使用原始使用者的 [*公開金鑰*](../secgloss/p-gly.md)[*交換金鑰*](../secgloss/e-gly.md)來加密新的工作階段金鑰，而這個新的金鑰可以替代為原始金鑰。 如果使用者在不知情的情況下使用替代的工作階段金鑰來加密檔案和訊息，則建立替代金鑰的人員可以輕鬆地將它們解密。

[雜湊和數位簽章](hashes-and-digital-signatures.md)中會詳細討論數位簽章。

 

 
