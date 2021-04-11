---
description: 映射完整性函式會管理影像檔案中的一組憑證。
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: 映射完整性函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025898"
---
# <a name="image-integrity-functions"></a>映射完整性函式

映射完整性函式會管理影像檔案中的一組憑證。 系統會提供常式來新增、移除和查詢憑證。 另外還有一個函式，可用來取得計算影像檔案摘要所需的影像檔位元組資料流程。 這是建立簽章憑證的必要項。

檔案中的每個憑證都有一個索引，可在移除憑證時變更。 新憑證一律會新增至現有憑證清單的「結尾」。 也就是說，它們的指派索引大於目前使用中的任何索引。 一般情況下，應用程式不應假設指定的憑證具有與其上次參考時相同的索引。

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



