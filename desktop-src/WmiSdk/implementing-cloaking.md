---
description: 「掩蓋」是模擬的延伸模組，可讓您更有效地控制 COM 如何透過 proxy 模擬用戶端。 如同許多形式的 WMI 安全性，您可以透過 CoSetProxyBlanket 和 CoInitializeSecurity 介面設定掩蓋。
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: 實施掩蓋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d32333250bc37d8ccbfdb17421fed635f0da77e6394229220b2b36a1ce57f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318893"
---
# <a name="implementing-cloaking"></a>實施掩蓋

「掩蓋」是模擬的延伸模組，可讓您更有效地控制 COM 如何透過 proxy 模擬用戶端。 如同許多形式的 WMI 安全性，您可以透過 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 介面設定掩蓋。

COM 提供下列形式的掩蓋：

-   靜態

    在第一次呼叫 proxy 時，COM 會依據執行緒或進程 token 來建立權杖識別。 如果您對 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)使用靜態掩蓋，請在 proxy 的存留期間設定 proxy 的身分識別。

-   動態

    COM 會在每次呼叫 proxy 時，重新建立執行緒或進程 token 中的權杖身分識別。 由於 COM 會在每次呼叫時檢查身分識別，因此動態擬呼可讓您更精確地控制用戶端身分識別。 不過，動態掩蓋的效率不如靜態的掩蓋。

當您設定與模擬委派層級的掩蓋時，伺服器可以跨伺服器傳播用戶端的身分識別，即使是在遠端伺服器也一樣。 如果您未啟用掩蓋，COM 會在實際的伺服器進程的環境下，從本機伺服器到遠端伺服器的任何呼叫。

「掩蓋」可讓 WMI 模擬用戶端跨多個電腦界限存取本機和遠端網路資源。 WMI 可以將用戶端的身分識別傳遞給本機和遠端伺服器，例如 WMI 的其他遠端實例。 然後，這些遠端伺服器就可以在初始用戶端內容下執行作業。

下列程式說明如何搭配使用掩蓋和委派。

**搭配使用掩蓋和委派**

1.  將驗證服務設定為 Kerberos。

    Kerberos 是唯一支援遠端掩蓋和委派的驗證服務。 這表示只有在遠端伺服器上才能使用「掩蔽」和「委派」。

2.  在 Active Directory 服務中，將伺服器登入帳戶標示為「受信任的委派」。
3.  在 Active Directory 服務中，將用戶端登入帳戶標示為「帳戶是機密的，無法委派」。

例如，呼叫 View 提供者可能會從多部電腦上的多個 WMI 實例傳回物件，可受益于委派和掩蓋。

 

 
