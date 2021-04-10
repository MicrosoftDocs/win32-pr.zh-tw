---
description: Microsoft RSA/Schannel 密碼編譯提供者支援雜湊、資料簽章和簽章驗證。
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Microsoft RSA/Schannel 密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9420849d62c0b728d8f3dbccc4210de3a1394308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943495"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Microsoft RSA/Schannel 密碼編譯提供者

Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md)密碼編譯提供者支援雜湊、資料簽章和簽章驗證。 演算法識別碼 CALG \_ SSL3 \_ SHAMD5 用於 SSL 3.0 和 TLS 1.0 用戶端驗證。 此 CSP 支援 SSL2、PCT1、SSL3 和 TLS1 通訊協定的金鑰衍生。 [*雜湊*](../secgloss/h-gly.md)是由 MD5 雜湊與 SHA 雜湊的串連所組成，並使用 RSA [*私密金鑰*](../secgloss/p-gly.md)進行簽署。 您可以將它匯出至其他國家/地區。



|                |                                  |
|----------------|----------------------------------|
| 提供者類型： | **>PROV \_ RSA \_ SCHANNEL**          |
| 提供者名稱： | **MS \_ DEF \_ RSA \_ SCHANNEL \_ >PROV** |



 

如需 RSA/Schannel 提供者的詳細資訊，請參閱 [CSP](cryptography-functions.md)函式。

 

 
