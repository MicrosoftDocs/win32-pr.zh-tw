---
title: 查詢簡單的許可權資訊
description: 查詢簡單的許可權資訊
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK，查詢簡易許可權
- Windows Media Format SDK，簡單許可權查詢
- 數位版權管理 (DRM) ，查詢簡單的許可權
- DRM (數位版權管理) ，查詢簡易許可權
- 數位版權管理 (DRM) 、簡單的許可權查詢
- DRM (數位版權管理) 、簡單的許可權查詢
- DRM 用戶端擴充 Api，查詢簡易許可權
- 用戶端擴充 Api，查詢簡易許可權
- DRM 用戶端擴充 Api，簡單許可權查詢
- 用戶端擴充 Api，簡單許可權查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372204"
---
# <a name="querying-for-simple-rights-information"></a>查詢簡單的許可權資訊

Windows Media DRM 用戶端擴充 Api 可讓您快速取得有關是否可針對各種動作存取受保護內容的簡單資訊。

[**IWMDRMLicenseQuery：： QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)方法可以用來快速判斷本機授權存放中的授權是否允許動作。 **QueryActionAllowed** 已經過優化，使用 Windows MEDIA 格式 SDK 的物件來查詢類似的資訊會比查詢更快。 不過，這種類型的查詢會匯總本機授權存放區中的授權，而且只能用於簡單的功能，例如使用者介面元素可能需要的，例如顯示許可權指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**從本機授權存放中的授權取得資訊**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




