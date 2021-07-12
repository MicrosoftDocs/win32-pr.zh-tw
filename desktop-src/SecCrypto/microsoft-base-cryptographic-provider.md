---
description: Microsoft 基礎密碼編譯提供者是 (CSP) 提供者的初始加密服務提供者，並與 CryptoAPI 版本1.0 和2.0 一起散發。 這是一般用途的提供者，可支援數位簽章和資料加密。
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Microsoft 基礎密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581886"
---
# <a name="microsoft-base-cryptographic-provider"></a>Microsoft 基礎密碼編譯提供者

Microsoft 基礎密碼編譯提供者是 (CSP) 提供者的初始 [*加密服務提供*](../secgloss/c-gly.md) 商，並與 [*CryptoAPI*](../secgloss/c-gly.md) 版本1.0 和2.0 一起散發。 這是一般用途的提供者，可支援 [*數位簽章*](../secgloss/d-gly.md) 和資料加密。

RSA 公開金鑰演算法可用於所有的公開金鑰作業。

為了維持與舊版的回溯相容性，新版的提供者會保留 Wincrypt 中名稱的1.0 指定。 不過，此提供者的2.0 版目前為出貨。 若要判斷使用中提供者的實際版本，請呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) ，並將 *dwParam* 引數設定為 **PP \_ 版本**。 如果在 *>pbdata* 中傳回0x0200，表示您的版本為2.0。

|                   | 值            |
|-------------------|------------------|
| **提供者類型** | >PROV \_ RSA \_ FULL  |
| **提供者名稱** | MS \_ DEF \_ >PROV    |



 

 

 
