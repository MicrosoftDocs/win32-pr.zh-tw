---
description: 從個人資訊安裝註冊的憑證 Exchange (PFX) 檔案儲存至憑證存放區。
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777604"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

installResponseFromPFX 範例會從個人資訊安裝註冊的憑證 Exchange (PFX) 檔加入至憑證存放區。

## <a name="location"></a>位置

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ installResponseFromPFX 資料夾中安裝範例。

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

 

 



