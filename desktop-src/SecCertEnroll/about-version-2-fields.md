---
description: X.509 版本 2 憑證包含版本 1 中定義的基本欄位，並新增下列欄位。
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: 第2版欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191117"
---
# <a name="version-2-fields"></a>第2版欄位

X.509 版本 2 憑證包含版本 1 中定義的基本欄位，並新增下列欄位。

## <a name="issuer-unique-identifier"></a>簽發者唯一識別碼

包含唯一識別碼，可以在一段時間後，當其他實體重複使用 CA 時，清楚識別該 CA 的 X.500 名稱。

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>主體唯一識別碼

包含唯一識別碼，可以在一段時間後，當其他實體重複使用憑證主體時，清楚識別該憑證主體的 X.500 名稱。

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本欄位](about-basic-fields.md)
</dt> <dt>

[第3版擴充功能](about-version-3-extensions.md)
</dt> <dt>

[X.509 公開金鑰憑證](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



