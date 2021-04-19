---
description: 驗證層級的協商
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: 驗證層級的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997072"
---
# <a name="negotiation-of-authentication-level"></a>驗證層級的協商

用戶端和伺服器都必須參與驗證，而且每個合作物件都表示它想要執行特定層級的驗證。 在呼叫開始時，會在兩個合作物件之間協商驗證層級、選擇適當的服務，並根據所) 選的驗證等級，進行驗證並繼續 (有可能的加密。 用戶端與伺服器之間協商的驗證層級會決定為最大 (*用戶端喜好* 設定，也就是 *伺服器喜好* 設定) 。 這表示伺服器隨時都可以決定最適合的驗證層級;也就是說，您可以從伺服器以系統管理員的身份進行驗證。

用戶端會指定它想要在特定層級執行驗證，就像使用任何 COM 應用程式一樣。 用戶端驗證等級可以指定如下：

-   每一部用戶端電腦，使用 [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) 或 [元件服務] 系統管理工具所設定的全電腦 COM 驗證等級。
-   根據用戶端應用程式，如果用戶端應該是 COM + 應用程式，則使用 [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) 或使用 [元件服務] 系統管理工具。
-   以程式設計方式，使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來處理每個用戶端。
-   在任何時間點以程式設計的方式使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)。

COM + 伺服器應用程式會使用 [元件服務] 系統管理工具 (或透過管理腳本) ，以系統管理員的方式指定驗證層級。

協商呼叫的驗證會依照下列順序進行：

1.   (*用戶端*、 *伺服器*) 的最大值選擇驗證等級。
2.  驗證通訊協定的協商。
3.  伺服器會驗證用戶端身分識別。
4.  （選擇性）用戶端會根據驗證通訊協定來驗證服務器身分識別。
5.  方法呼叫會與所選的驗證層級進行通訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> </dl>

 

 
