---
description: 安全通道通訊協定需要認證，以驗證服務器和用戶端（選擇性）。
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944132"
---
# <a name="schannel-credentials"></a>Schannel 認證

安全通道通訊協定需要認證，以驗證服務器和用戶端（選擇性）。 [*安全通道安全性通訊協定*](../secgloss/s-gly.md)需要伺服器驗證（伺服器會將其身分識別證明提供給用戶端）。 伺服器可能會在任何時間要求用戶端驗證。

Schannel 認證是 [*x.509*](../secgloss/x-gly.md) 憑證。 憑證的 [*公開*](../secgloss/p-gly.md)和 [*私密金鑰*](../secgloss/p-gly.md)資訊可用來驗證服務器和用戶端（選擇性）。 當用戶端和伺服器交換產生和交換 [*工作階段金鑰*](../secgloss/s-gly.md)所需的資訊時，也會使用這些金鑰來提供訊息 [*完整性*](../secgloss/i-gly.md)。

如需程式設計資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。

 

 
