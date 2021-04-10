---
description: 支援數位簽章和資料加密。 它被視為一般用途密碼編譯服務提供者 (CSP) 。
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027178"
---
# <a name="prov_rsa_aes"></a>>PROV \_ RSA \_ AES

>PROV \_ RSA \_ AES 提供者類型支援 [數位簽章](digital-signatures.md) 和資料加密。 它被視為一般用途 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。 RSA [*公開金鑰演算法*](../secgloss/p-gly.md) 可用於所有的 [*公開金鑰*](../secgloss/p-gly.md) 作業。

## <a name="algorithms-supported"></a>支援的演算法

如需這些演算法的說明，請參閱詞彙。



| 目的      | 支援的演算法                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 金鑰交換 | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| 簽名    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| 加密   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*進階加密標準*](../secgloss/a-gly.md) (AES)  <br/>                                                       |
| 雜湊      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-1 (256 SHA-1、SHA-384 和 SHA-512) <br/> |



 

## <a name="related-documentation"></a>相關文件

此提供者類型是由 Microsoft 和 RSA 資料安全性所定義。 本檔將在下列檔中說明：

-   *Microsoft 密碼編譯服務提供者程式設計人員指南*，microsoft，1996。
-   RSA 實驗室，公開金鑰加密標準，RSA 資料安全性，1993年11月。

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
