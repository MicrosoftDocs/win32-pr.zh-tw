---
title: 查詢詳細的許可權資訊
description: 查詢詳細的許可權資訊
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows媒體格式 SDK，查詢詳細許可權
- Windows媒體格式 SDK，詳細的許可權查詢
- 數位版權管理 (DRM) ，查詢詳細權利
- DRM (數位版權管理) ，查詢詳細權利
- 數位版權管理 (DRM) ，詳細的許可權查詢
- DRM (數位版權管理) ，詳細的許可權查詢
- DRM 用戶端擴充 Api，查詢詳細許可權
- 用戶端擴充 Api，查詢詳細許可權
- DRM 用戶端擴充 Api、詳細的許可權查詢
- 用戶端擴充 Api、詳細的許可權查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff27904686016870151dbf91affc7c4e5241a9ae9fef02b86a5786fe1f5d506d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084516"
---
# <a name="querying-for-detailed-rights-information"></a>查詢詳細的許可權資訊

藉由使用 [**IWMDRMLicenseQuery：： QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) 方法，您可以取得金鑰識別碼授權所授與之許可權的詳細資訊。 從這個方法取得的資訊，會從套用至指定金鑰識別碼的本機授權存放區中的所有授權進行匯總。

**QueryLicenseState** 使用 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md) 結構來顯示指定金鑰識別碼的所有授權相關匯總資訊。 此使用方式與 Windows 媒體格式 SDK 中的其他物件不同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**從本機授權存放中的授權取得資訊**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




