---
title: ASF 承載解密和重新加密
description: ASF 承載解密和重新加密
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Media 格式 SDK、ASF 承載解密和重新加密
- Windows Media Format SDK、承載解密和重新加密
- Windows Media Format SDK，解密
- Windows Media Format SDK，重新加密
- 數位版權管理 (DRM) 、ASF 承載解密和重新加密
- DRM (數位版權管理) 、ASF 承載解密和重新加密
- 數位版權管理 (DRM) 、承載解密和重新加密
- DRM (數位版權管理) 、承載解密和重新加密
- 數位版權管理 (DRM) 、解密
- DRM (數位版權管理) 、解密
- 數位版權管理 (DRM) ，重新加密
- DRM (數位版權管理) ，重新加密
- DRM 用戶端擴充 Api、ASF 承載解密和重新加密
- 用戶端擴充 Api、ASF 承載解密和重新加密
- DRM 用戶端擴充 Api、承載解密和重新加密
- 用戶端擴充 Api、承載解密和重新加密
- DRM 用戶端擴充 Api，解密
- 用戶端擴充 Api，解密
- DRM 用戶端擴充 Api，重新加密
- 用戶端擴充 Api，重新加密
- Advanced Systems Format (ASF) 、重新加密
- ASF (Advanced Systems Format) ，重新加密
- Advanced Systems Format (ASF) 、解密
- ASF (Advanced Systems Format) 、解密
- Advanced Systems Format (ASF) 、承載解密和重新加密
- ASF (Advanced 系統格式) 、承載解密和重新加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671444"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>ASF 承載解密和重新加密

下列步驟描述應用程式必須完成才能解密和重新加密每個承載的動作：

1.  遞增 salt 值。
2.  傳遞 (以 Windows Media DRM) 加密的承載，並將 salt 值傳遞給解密函式 [**IWMDRMDecrypt：:D ecrypt**](iwmdrmdecrypt-decrypt.md)，這會傳回使用 RC4 公開金鑰加密的承載。
3.  藉由套用與 salt 值串連之初始化向量的 SHA-1 雜湊，來衍生暫時性的 RC4 金鑰。
4.  使用您的暫時性金鑰來解密承載。
5.  根據 Windows Media DRM 匯出合規性和穩定性規則，以授權的內容保護設定立即重新加密承載。
6.  找出下一個承載。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**匯出壓縮的內容**](exporting-compressed-content.md)
</dt> </dl>

 

 




