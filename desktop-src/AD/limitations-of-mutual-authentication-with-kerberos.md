---
title: 使用 Kerberos 進行相互驗證的限制
description: 用戶端的帳戶和服務的帳戶必須在 Windows 2000 原生或混合模式網域中，因為在舊版網域中無法使用 Kerberos 服務。
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462016"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>使用 Kerberos 進行相互驗證的限制

用戶端的帳戶和服務的帳戶必須在 Windows 2000 原生或混合模式網域中，因為在舊版網域中無法使用 Kerberos 服務。 此外，用戶端和服務帳戶都必須位於相同的樹系中，因為用戶端的 KDC 會使用通用類別目錄來搜尋服務主體名稱。

服務和用戶端都必須在 Windows 2000 上執行，否則 Kerberos 的相互驗證將會失敗，因為舊版 Windows 不支援 Kerberos。

服務主體名稱必須包含執行服務之主機伺服器的 DNS 名稱。 您必須使用 DNS 名稱。

 

 




