---
description: 加密是指將純文字資料 (純文字) 轉換成看似隨機且無意義 (加密文字) 的程式。 解密是將加密文字轉換回純文字的程式。
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: 資料加密和解密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba508eeb67570d1f293ae55e1b6bff5217529663a6682a17d9817a9dc0834803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100908"
---
# <a name="data-encryption-and-decryption"></a>資料加密和解密

加密是指將純文字資料 ([*純*](../secgloss/p-gly.md) 文本) 轉換成看似隨機且無意義 ([*加密*](../secgloss/c-gly.md) 文字) 的程式。 解密是將加密文字轉換回純文字的程式。

若要加密超過少量的資料，請使用 [*對稱式加密*](../secgloss/s-gly.md) 。 [*對稱金鑰*](../secgloss/s-gly.md)是在加密和解密程式期間使用。 若要將特定的加密文字片段解密，必須使用用來加密資料的金鑰。

每個加密演算法的目標是要讓它盡可能難以解密所產生的加密文字，而不使用金鑰。 如果使用的是很好的加密演算法，則在每個可能的索引鍵中，都不會有明顯的技巧。 針對這樣的演算法，索引鍵越長，就越難解密加密文字片段，而不需要擁有金鑰。

很難判斷加密演算法的品質。 如果有適當的攻擊，則看起來的演算法有時會很容易中斷。 選取加密演算法時，最好選擇已在使用中的帳戶，並成功 resisted 所有攻擊。

如需詳細資訊，請參閱 [資料加密和解密功能](cryptography-functions.md)。

 

 
