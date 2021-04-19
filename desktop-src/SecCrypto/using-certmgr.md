---
description: 使用 Certmgr.msc 從檔案或憑證存放區中查看憑證、Crl 和 Ctl、將憑證複製到憑證存放區、從憑證存放區刪除憑證，以及將憑證儲存至檔案。
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: 使用 Certmgr.msc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974553"
---
# <a name="using-certmgr"></a>使用 Certmgr.msc

[Certmgr.msc](certmgr.md) 可以用來查看 [*憑證*](../secgloss/c-gly.md)、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 和 [*憑證信任清單*](../secgloss/c-gly.md) (ctl) 自檔案或憑證存放區、將憑證複製到 [*證書*](../secgloss/c-gly.md)存儲、從憑證存放區刪除憑證，以及將憑證儲存至檔案。

當使用 [certmgr.msc](certmgr.md) 時沒有選項時，會出現 certmgr.msc wizard 來引導使用者完成此操作。

檔案必須是下列其中一種類型：

-   編碼的 CTL、CRL 或憑證檔案 (可以是以64為基礎的編碼) 
-   PKCS \# 7 檔案
-   SPC 檔案
-   簽署的檔
-   序列化的 storeFile

下列範例會使用 [certmgr.msc](certmgr.md) 命令來執行一般的憑證工作。

-   從 *myfile.txt* 查看憑證、Crl 和 ctl。

    **Certmgr.msc** *myfile.txt ext*

-   從 [我的系統] 存放區查看憑證、Crl 和 Ctl。

    **certmgr.msc-s**

-   將名為 *myfile.txt* 的檔案中的所有憑證、Crl 和 ctl 複製到稱為 *NewFile* 的新檔案中。

    **certmgr.msc-add-all-c** *myfile.txt.* *ext*

-   將 [我的系統] 存放區中的所有憑證、Crl 和 Ctl 複製到名為 *NewMyFile* 的檔案。

    **certmgr.msc-add-all-c-s my** *NewMyFile ext*

-   將 [我的系統] 存放區中的一般名稱 *mycert.cer* 的憑證複製到名為 *NewCert* 的檔案。

    **certmgr.msc-add-c-n** *mycert.cer* **-s my** *NewCert .cer*

-   刪除 [我的系統] 存放區中的所有憑證。

    **certmgr.msc-del-全部-c-s**

-   刪除 [我的系統] 存放區中的所有 Ctl，然後將產生的存放區儲存到名為 *NewStore* 的檔案。

    **certmgr.msc-del-all-ctl-s my** *NewStore*

-   儲存至名為 *NewCert* 的檔案，這是 [*x.509*](../secgloss/x-gly.md) 編碼憑證的憑證，其具有一般名稱 *mycert.cer*，且位於根憑證存放區中。

    **certmgr.msc-put-c-n** *mycert.cer* **-s root** *NewCert .cer*

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Certmgr.msc](certmgr.md)
</dt> </dl>

 

 
