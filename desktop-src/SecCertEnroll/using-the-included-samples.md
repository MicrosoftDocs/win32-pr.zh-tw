---
description: '憑證註冊 API 包含多個範例，其設計目的是要協助您建立自訂應用程式。 大部分的範例都是使用 c + + 撰寫的，但 c # 和 Visual Basic 腳本 Edition (VBScript) 範例也包含在內。'
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: 使用包含的範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511d9d5424455c1b54c6bd03cc72138b3672b256d535dcbdaf31d2393b2cb5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127200"
---
# <a name="using-the-included-samples"></a>使用包含的範例

憑證註冊 API 包含多個範例，其設計目的是要協助您建立自訂應用程式。 大部分的範例都是使用 c + + 撰寫的，但 c # 和 Visual Basic 腳本 Edition (VBScript) 範例也包含在內。

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ 資料夾中安裝下列範例。



| 範例                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                | 語言            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | 從內部的嵌套 PKCS 10 要求建立 CMC 要求物件 \# 。<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | 包含下列提供的範例所使用的 helper 函式和宏。<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | 建立 CMC 憑證要求，並在憑證階層中註冊電腦。<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | 建立自訂的 PKCS \# 10 要求、將它提交給獨立的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位（ (CA) ），並在 [*憑證存放區*](/windows/desktop/SecGloss/c-gly)中安裝已發行的憑證。<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | 建立自訂的 PKCS \# 10 要求，並嘗試在企業 CA 中進行註冊。<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | 代表另一位使用者建立 CMC 憑證要求，並在證書階層中註冊使用者。<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | 初始化 PKCS \# 10 憑證要求物件、將其包裝在 CMC 要求物件中、將 CMC 要求提交至企業 CA，並將 CA 傳回的憑證儲存在檔案中。<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | 建立 CMC 憑證要求，以封存 CA 上的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 。<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | 從檔案讀取現有的 CMC 憑證要求、將其包裝在另一個 CMC 要求中、簽署此外部要求、將它提交給 CA，然後將憑證回應儲存至檔案。<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | 藉由繼承公開金鑰和私密金鑰和憑證範本，從現有的憑證建立 [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) 要求。 此範例會在憑證階層中註冊使用者，並安裝憑證回應。<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | 建立 PKCS \# 7 要求物件以更新現有的憑證。<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | 使用範本、憑證顯示名稱和憑證描述，在證書階層中註冊電腦。<br/>                                                                                                                                                                                                                 | C + +、VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | 使用範本、主體名稱和金鑰的長度（以位為單位），向 CA 註冊使用者。<br/>                                                                                                                                                                                                                                       | C + +、C#<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | 示範如何使用 Windows 7 HTTP 通訊協定在企業 CA 註冊憑證。<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | 從個人資訊安裝註冊的憑證 Exchange (PFX) 檔案儲存至憑證存放區。<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用憑證註冊 API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

