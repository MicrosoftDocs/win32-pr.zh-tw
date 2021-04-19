---
description: 建立 CMC 憑證要求，以在憑證授權單位單位 (CA) 封存私密金鑰。
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974078"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

EnrollKeyArchivalCMC 範例會建立 CMC 憑證要求，以在憑證授權單位單位 (CA) 封存私密金鑰。 如需詳細資訊，請參閱 [CMC 金鑰保存要求](cmc-key-archival-request.md)。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollKeyArchivalCMC 資料夾中。

## <a name="discussion"></a>討論

EnrollKeyArchivalCMC 範例：

1.  處理命令列引數。 命令列應包含用於註冊的憑證範本名稱。
2.  使用範本名稱，建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 憑證要求物件，並將其初始化為終端使用者內容。
3.  設定 CMC 要求的 [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) 屬性。
4.  建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。
5.  建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它來取得 CA 的 exchange 憑證。
6.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件、使用 CMC 要求進行初始化、建立包含金鑰封存要求的 base64 編碼字串，並將它提交給 CA。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 金鑰封存要求](cmc-key-archival-request.md)
</dt> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 
