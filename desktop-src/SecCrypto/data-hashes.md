---
description: 文字或其他位元組字串的雜湊是相關的、統計唯一、固定長度的值。
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: 資料雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852311"
---
# <a name="data-hashes"></a>資料雜湊

文字或其他位元組字串的 [*雜湊*](../secgloss/h-gly.md) 是相關的、統計唯一、固定長度的值。 在某些檔中，文字的 *雜湊* 也稱為摘要;不過，在本檔中，一律會使用「雜湊」一詞。 CryptoAPI 函式提供一種方法來建立任何文字或其他位元組字串的雜湊。 然後，該雜湊就可以用來作為其相關資料的唯一識別碼。

為了確保文字的 [*完整性*](../secgloss/i-gly.md) ，文字的 [*雜湊*](../secgloss/h-gly.md) 可以隨文字一起傳送。 然後接收者可以計算所收到資料的雜湊，並比較以接收的雜湊計算的雜湊。 如果兩者相符，則接收的資料必須與建立所接收雜湊的資料相同。

若要取得雜湊值，請使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)建立雜湊物件。 此物件將累積要驗證的資料。 然後使用 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) 函式，將資料新增至雜湊物件。

將最後一個資料區塊新增至雜湊之後， [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) 函數會用來取得資料的雜湊值。

一旦取得雜湊值，就會以 [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) 終結雜湊物件，以提供更佳的安全性。

 

 
