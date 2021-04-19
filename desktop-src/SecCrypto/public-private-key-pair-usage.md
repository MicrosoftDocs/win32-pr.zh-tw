---
description: 所有一般的 RSA/Schannel 和 Diffie-hellman/安全通道作業都會使用 AT \_ KEYEXCHANGE 公開/私密金鑰組。
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: 公開/私密金鑰組使用方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000302"
---
# <a name="publicprivate-key-pair-usage"></a>公開/私密金鑰組使用方式

所有一般的 [*RSA*](../secgloss/r-gly.md)/Schannel 和 [*diffie-hellman*](../secgloss/d-gly.md)/SCHANNEL 作業都會使用 AT \_ KEYEXCHANGE [*公開/私密金鑰*](../secgloss/p-gly.md)組。 為了提供伺服器 [*驗證*](../secgloss/a-gly.md)，Schannel 作業的伺服器端必須能夠存取其 [*x.509*](../secgloss/x-gly.md) 憑證，其中包含其公開金鑰和相符 [*私密金鑰*](../secgloss/p-gly.md)的存取權。 如果執行用戶端驗證，則 [*Schannel*](../secgloss/s-gly.md) 的用戶端需要其公開金鑰和其私密金鑰的存取權。

因為安全通道通訊協定引擎絕不會使用 AT \_ SIGNATURE 公開/私密金鑰組，所以僅支援 RSA/schannel 或 diffie-hellman/schannel 的新 CSP 不需要支援該金鑰組。

如果通訊協定引擎使用的 SSL 3.0 匯出加密套件的 \_ KEYEXCHANGE 金鑰組大於512個位，則伺服器必須使用額外的 RSA 金鑰組。 這項額外的金鑰組一律為512位，而且可能是暫時的。 此配對會儲存為 \_ 通訊協定引擎所擁有之金鑰容器中的 KEYEXCHANGE 元素。 在通訊協定引擎啟動時，通常會取得此金鑰容器的控制碼。

Diffie-Hellman 只支援 [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) ，並使用一般的 RSA 或 DSS 公開金鑰。

 

 
