---
description: 不透明的 Blob （也稱為 OPAQUEKEYBLOBs）是用來將工作階段金鑰儲存為特定廠商的格式，例如 Schannel。
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: 不透明的 BLOB 類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386279"
---
# <a name="opaque-blob-type"></a>不透明的 BLOB 類型

不 [*透明的 blob*](../secgloss/o-gly.md)（也稱為 OPAQUEKEYBLOBs）是用來將 [*工作階段金鑰*](../secgloss/s-gly.md)儲存為特定廠商的格式，例如 [*Schannel*](../secgloss/s-gly.md)。 其中包含基本金鑰材質和所有目前的 [*狀態*](../secgloss/s-gly.md) 資訊。 這包括 [*salt 值*](../secgloss/s-gly.md)、 [*初始化向量*](../secgloss/i-gly.md)和索引鍵資料表等資訊。 不透明 Blob 的格式已解除發佈。 每個 CSP 廠商都會決定自己的 BLOB 格式。

因為金鑰會匯出為 CSP 專屬格式的不透明 BLOB，所以只能匯入其原本匯出的 CSP 中。

牽涉到兩個進程時，每個 [*進程*](../secgloss/p-gly.md) 都會個別呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 。 每個進程都會取得金鑰容器的控制碼。 這兩個處理常式都有可能會有相同金鑰容器的控制碼。 其中一個進程會建立金鑰，並將它們匯出到不透明的 Blob，然後將 Blob 傳遞給第二個進程。 第二個進程會將 BLOB 中的金鑰匯入至其 [*金鑰容器*](../secgloss/k-gly.md)。

如果硬體 CSP 不支援匯出金鑰，BLOB 可能只會包含金鑰登錄的索引或類似的索引。 在此情況下，會忽略程式的其餘部分。

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
