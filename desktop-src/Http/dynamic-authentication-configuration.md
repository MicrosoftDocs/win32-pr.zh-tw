---
title: 動態驗證設定
description: 應用程式可以隨時變更 URL 群組或伺服器會話的驗證設定。
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014836"
---
# <a name="dynamic-authentication-configuration"></a>動態驗證設定

根據預設，HTTP 伺服器 API 不會執行驗證，除非應用程式明確啟用它。 應用程式可以隨時變更 URL 群組或伺服器會話的驗證設定。 驗證設定的變更不會影響已經過驗證或正在分派至應用程式的要求

針對需要多次交握的驗證配置，如果目前的配置因為應用程式的設定變更而不再受支援，則 HTTP 伺服器 API 會卸載驗證交握。 例如，如果應用程式啟用 Negotiate 並停用 NTLM，而 HTTP 伺服器 API 在 NTLM 的中繼驗證交握中，則會捨棄 NTLM 的交握，並將要求傳遞至應用程式。 應用程式會使用 WWW-Authenticate 標頭中指定的新驗證類型來傳送401驗證挑戰。

 

 




