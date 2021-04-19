---
description: 列出封套資料之功能的變更。
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: 新增封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982370"
---
# <a name="enveloped-data-additions"></a>新增封包資料

已對封包資料功能進行下列變更：

-   收件者識別不僅可以透過簽發者和序號 (PKCS \# 7 1.5) ，也可以透過金鑰識別碼來完成。
-   提供三個收件者金鑰交換選項：
    -   使用 RSA 金鑰的金鑰傳輸。
    -   使用 Ephemeral-Static Diffie-Hellman 以3DES 或 RC2 包裝之演算法金鑰的金鑰協定，或 Ephemeral-Static 橢圓曲線 Diffie-Hellman 以 AES 包裝的演算法金鑰。
    -   金鑰加密金鑰或郵寄清單金鑰傳送，用來加密內容加密金鑰的金鑰已發佈至收件者。 RC2、3DES 和 AES 可以作為金鑰包裝演算法。
-   未受保護的屬性可以包含在訊息中。
-   已新增 **OriginatorInfo** 欄位，其中包含建立者的相關資訊，其中可包含憑證和 crl。
-   橢圓曲線密碼編譯 (ECC) 演算法和 AES 需要 Windows Vista 或更新版本。

 

 



