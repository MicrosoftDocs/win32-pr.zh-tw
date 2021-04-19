---
description: 說明如何手動驗證安全通道認證。
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: 手動驗證 Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998142"
---
# <a name="manually-validating-schannel-credentials"></a>手動驗證 Schannel 認證

根據預設，Schannel 會藉由呼叫 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)函數來驗證 [*伺服器憑證*](../secgloss/s-gly.md);但是，如果您已使用「ISC 要求手動認證驗證」旗標來停用這項功能 \_ \_ \_ \_ ，就必須驗證嘗試建立其身分識別的伺服器所提供的憑證。

若要手動驗證伺服器憑證，您必須先取得伺服器憑證。 使用 [**QueryCoNtextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) 函數，並指定 SECPKG \_ ATTR \_ REMOTE \_ CERT \_ CONTEXT 屬性值。 這個屬性會傳回 [**憑證 \_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) 結構，其中包含伺服器所提供的憑證。 此憑證稱為分葉憑證，因為它是憑證鏈中的最後一個憑證，而且離 [*跟憑證*](../secgloss/r-gly.md)的距離最遠。

使用分葉憑證時，您必須確認下列各項：

-   憑證鏈已完成，根是信任的 [*憑證授權單位*](../secgloss/c-gly.md) 單位的憑證 (CA) 。
-   目前的時間不超過憑證鏈中每個憑證的開始和結束日期。
-   憑證鏈中的憑證都沒有被撤銷。
-   分葉憑證的深度不會比憑證延伸中指定的最大允許深度更深入。 只有當指定了深度時，才需要進行這項檢查。
-   憑證的使用方式正確，例如，不應該使用 [*用戶端憑證*](../secgloss/c-gly.md) 來驗證服務器。
-   針對伺服器驗證，包含在伺服器之分葉憑證中的伺服器身分識別，與用戶端嘗試聯絡的伺服器相符。 一般而言，用戶端會將憑證的 [主體名稱] 欄位中的某個專案與伺服器的 IP 位址或 DNS 名稱進行比對。

 

 
