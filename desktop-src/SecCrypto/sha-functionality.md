---
description: 原始的基底提供者錯誤地報告了 SHA 雜湊演算法，其會呼叫 CryptGetProvParam 並指定參數 PP ENUMALGS 來列舉演算法 \_ 。
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: SHA 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689456"
---
# <a name="sha-functionality"></a>SHA 功能

原始的基底提供者錯誤地報告了 [*SHA*](../secgloss/s-gly.md) 雜湊演算法，其會呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) 並指定參數 PP ENUMALGS 來列舉演算法 \_ 。 這已在基底提供者中修正。 修訂的基底提供者和延伸的提供者，現在都能正確地報告 SHA-1。

已將已定義的 CALG \_ SHA1 常數新增至 Wincrypt，其值與 CALG SHA 相同 \_ 。

 

 
