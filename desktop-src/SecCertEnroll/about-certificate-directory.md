---
description: Windows 公開金鑰基礎結構 (PKI) 將憑證儲存在裝載證書 (頒發機構單位的伺服器上) 以及本機電腦或裝置上。
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: 憑證目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195410"
---
# <a name="certificate-directory"></a>憑證目錄

Windows 公開金鑰基礎結構 (PKI) 將憑證儲存在裝載證書 (頒發機構單位的伺服器上) 以及本機電腦或裝置上。 CA 儲存體通常稱為憑證資料庫，而本機儲存體則稱為「憑證存放區」。

## <a name="certificate-database"></a>憑證資料庫

當您在 Windows server 上新增憑證服務並設定 CA 時，會建立憑證資料庫。 根據預設，資料庫會包含在 *% SystemRoot%* \\ System32 \\ Certlog 資料夾中，而且名稱會以 .edb 副檔名的 CA 名稱為基礎。 資料庫可包含：

-   發行的憑證
-   撤銷的憑證
-   封存的私密金鑰
-   憑證要求

您無法使用憑證註冊 API 來運算元據庫。 註冊程式會自動建立所需的專案。

## <a name="certificate-stores"></a>憑證存放區

Microsoft 憑證服務會將發出的憑證和擱置或拒絕的要求複製到本機電腦和裝置。 儲存位置稱為憑證存放區，並由下列邏輯存放區所組成。

| 邏輯存放區                                         | Description                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 個人<br/>                                   | 包含與使用者或電腦所控制之私密金鑰相關聯的憑證。<br/>                     |
| 可信任的根憑證授權單位<br/>     | 包含隱含信任的憑證授權單位單位)  (Ca 的憑證。<br/>                              |
| 企業信任<br/>                           | 包含通常用來信任來自其他組織之自我簽署憑證的憑證信任清單。<br/> |
| 中繼憑證授權單位<br/>     | 包含對證書階層中的次級 Ca 發出的憑證。<br/>                             |
| Active Directory 使用者物件<br/>               | 包含 Active Directory 中發佈的使用者物件憑證或憑證。<br/>                         |
| 受信任的發行者<br/>                         | 包含來自信任的 Ca 的憑證。<br/>                                                                     |
| 未受信任的憑證<br/>                     | 包含已明確識別為未受信任的憑證。<br/>                                    |
| 第三方根憑證授權單位<br/> | 包含來自內部憑證階層以外之 Ca 的受信任根憑證。<br/>                     |
| 受信任的人<br/>                             | 包含發給已明確信任之使用者或實體的憑證。<br/>                        |
| 其他人<br/>                               | 包含發給已隱含信任之使用者或實體的憑證。<br/>                        |
| 憑證註冊要求<br/>            | 包含暫止或已拒絕的憑證要求。<br/>                                                          |



 

您無法使用憑證註冊 API 來指定或抓取存放區屬性，或將憑證複製到特定存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKI 元素](about-pki-components.md)
</dt> </dl>

 

 




