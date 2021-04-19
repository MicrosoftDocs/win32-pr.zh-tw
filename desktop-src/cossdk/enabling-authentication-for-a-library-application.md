---
description: 啟用程式庫應用程式的驗證
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: 啟用程式庫應用程式的驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972142"
---
# <a name="enabling-authentication-for-a-library-application"></a>啟用程式庫應用程式的驗證

由於 COM + 程式庫應用程式是由其他進程主控，因此其安全性需求可能與伺服器應用程式的需求不同。 如果程式庫應用程式將由瀏覽器主控，則可能需要接收未經驗證的回呼。

若要解決此需求，您可以停用驗證，讓裝載進程不會針對程式庫應用程式的呼叫端執行安全性檢查。 當您停用驗證時，對程式庫應用程式的呼叫會有效地進行未經驗證，而且所有對它的呼叫都會成功。 如需詳細資訊，請參閱連結 [庫應用程式安全性](library-application-security.md)。

**啟用 (或停用程式庫應用程式的) 驗證**

1.  以滑鼠右鍵按一下您要啟用或停用驗證的 COM + 應用程式，然後按一下 [ **屬性**]。

2.  在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

3.  在 [ **驗證**] 下，選取 [ **啟用驗證** ] 核取方塊以啟用驗證;清除此核取方塊將會停用驗證。

4.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



