---
description: 用戶端和伺服器憑證都必須儲存在應用程式進程可存取的憑證存放區中。
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: 憑證存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026501"
---
# <a name="certificate-stores"></a>憑證存放區

[*用戶端*](/windows/desktop/SecGloss/c-gly)和 [*伺服器憑證*](/windows/desktop/SecGloss/s-gly)都必須儲存在應用程式進程可存取的 [*憑證存放區*](/windows/desktop/SecGloss/c-gly)中。 一般而言，這是「我的存放區」，也稱為「個人」存放區。 像 Internet Explorer 的用戶端應用程式通常會使用目前使用者的「我的存放區」，而伺服器（例如 Internet Information Services (IIS) 使用本機電腦的「系統」存放區。

當 Schannel 或應用程式建立要傳送至遠端電腦的憑證鏈時，會使用根存放區和 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 存放區。 這些存放區用來驗證已接收的憑證鏈。 如需詳細資訊，請參閱 [使用 Schannel 執行驗證](performing-authentication-using-schannel.md)。

 

 
