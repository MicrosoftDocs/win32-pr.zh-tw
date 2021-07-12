---
description: Cert2spc.exe
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2spc.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581976"
---
# <a name="cert2spc"></a>Cert2spc.exe

cert2spc.exe 工具會使用現有的 [*x.509*](../secgloss/x-gly.md) [*憑證*](../secgloss/c-gly.md)， [*Publisher 憑證*](../secgloss/s-gly.md) (SPC) 建立測試軟體。 Cert2spc.exe 可將多個 x.509 憑證包裝到 [*PKCS \# 7*](../secgloss/p-gly.md) 的已簽署資料物件中。 此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。

cert2spc.exe 可做為 Windows SDK 的一部分，可供您下載 <https://go.microsoft.com/fwlink/p/?linkid=84091> 。

> [!Note]
> 此工具僅供測試之用。 從 [*憑證授權單位*](../secgloss/c-gly.md)單位取得有效的 SPC。


**Cert2spc.exe** *Cert1 .cer Cert2 .cer* .。。 *輸出 spc*

 



| 參數              | 描述                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1 .Cer Cert2 .cer* .。。 | 要包含在 SPC 中的 x.509 憑證名稱。 每個憑證名稱的結尾都是 .cer 副檔名。                         |
| *輸出 spc*            | PKCS \# 7 物件的名稱，其中包含要建立的 x.509 憑證。 輸出檔名稱以 .spc 副檔名結尾。 |



 

 

 
