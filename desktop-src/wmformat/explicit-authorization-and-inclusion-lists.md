---
title: 明確授權和包含清單
description: 明確授權和包含清單
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows媒體格式 SDK，DRM 匯出
- Windows媒體格式 SDK，匯出
- Windows媒體格式 SDK、明確授權和包含清單
- Windows媒體格式 SDK，授權清單
- Windows媒體格式 SDK，包含清單
- 數位版權管理 (DRM) 、匯出
- DRM (數位版權管理) ，匯出
- 數位版權管理 (DRM) 、明確授權和包含清單
- DRM (數位版權管理) 、明確授權和包含清單
- 數位版權管理 (DRM) 、授權清單
- DRM (數位版權管理) 、授權清單
- 數位版權管理 (DRM) ，包含清單
- DRM (數位版權管理) ，包含清單
- DRM 用戶端擴充 Api、明確授權和包含清單
- 用戶端擴充 Api、明確授權和包含清單
- DRM 用戶端擴充 Api、授權清單
- 用戶端擴充 Api、授權清單
- DRM 用戶端擴充 Api，包含清單
- 用戶端擴充 Api，包含清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee489d91002cacf7d8a0c89ffeef1752cd844aa089fabbe636e5e50fc185a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089728"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>明確授權和包含清單

授權可包含包含清單，以明確授權將受 Windows 媒體 DRM 保護的內容匯出至 (CPS) 的其他內容保護設定。 根據您在 Microsoft 輸入的許可合約條款來啟用 DRM 匯出，您只能匯出到授權包含清單中所識別的有效 CPS。

包含清單是全域唯一識別碼 (Guid 的系結陣列，) 每個都代表可匯出內容的特定授權 CPS。 包含清單中列出的 Guid 與輸出保護層級無關， (OPL) 和內容保護層級 (CPL) 。 強制執行這些限制是您的應用程式的責任。

> [!Note]  
> 在壓縮的內容上執行 Windows 媒體 DRM 匯出時，您可以透過 [**IWMDRMLicense：： GetInclusionList**](iwmdrmlicense-getinclusionlist.md)方法存取包含清單。 在未壓縮的內容上執行 Windows 媒體 DRM 匯出時，請使用 [**IWMDRMReader3：： GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist)方法。

 

若要在 Windows 媒體 drm 匯出合規性規則中，將新的內容保護系統註冊為 Windows 媒體 drm 允許匯出，請聯絡 wmla@microsoft.com 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯出**](drm-export.md)
</dt> </dl>

 

 




