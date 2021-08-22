---
description: 使用雜湊和數位簽章函式時，使用者可以數位方式簽署資料，讓其他使用者可以確認資料在簽署後尚未變更。 也可以驗證簽署資料之使用者的身分識別。
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: 雜湊和數位簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006486"
---
# <a name="hashes-and-digital-signatures"></a>雜湊和數位簽章

使用 [雜湊和數位簽章](cryptography-functions.md)函式時，使用者可以數位方式簽署資料，讓其他使用者可以確認資料在簽署後尚未變更。 也可以驗證簽署資料之使用者的身分識別。

[*數位簽章*](../secgloss/d-gly.md)是由少量的二進位資料所組成，通常少於256個位元組。 此簽章可以與已簽署的訊息配套或個別儲存，視特定應用程式的執行方式而定。

Microsoft 強式密碼編譯提供者會建立符合 RSA [*公開金鑰加密標準*](../secgloss/p-gly.md) (PKCS) 1 的數位簽章 \# 。

 

 
