---
description: 從個人資訊交換將已註冊的憑證 (PFX) 檔案安裝至憑證存放區。
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944959"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

InstallResponseFromPFX 範例會將個人資訊交換 (PFX) 檔案中的已註冊憑證安裝至憑證存放區。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ installResponseFromPFX 資料夾中。

## <a name="discussion"></a>討論

InstallResponseFromPFX 範例：

1.  處理命令列引數。 命令列應該包含：
    -   範例的名稱。
    -   包含已註冊憑證之 PFX 檔案的名稱。
    -   與 PFX 檔案相關聯的密碼。
2.  讀取 PFX 檔案，如果 base64 失敗，則先嘗試 base64 格式，以及二進位格式。 DecodeFileW () 函式定義于 enrollCommon .cpp 中。
3.  將已註冊的憑證轉換成 **BSTR** ，並用它來初始化 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件。 ConvertWszToBstr 函式定義于 enrollCommon .cpp 中。
4.  將憑證安裝在憑證存放區中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



