---
title: 在本機建立授權
description: 在本機建立授權
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows媒體格式 SDK，在本機建立授權
- Windows媒體格式 SDK，授權
- 數位版權管理 (DRM) ，在本機建立授權
- DRM (數位版權管理) ，在本機建立授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，在本機建立授權
- 用戶端擴充 Api，在本機建立授權
- 授權，在本機建立授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1a889e83f093cbd60043b299b7174a6c963663962a66454c5707060e76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433904"
---
# <a name="creating-licenses-locally"></a>在本機建立授權

在某些情況下，例如 [DRM 匯入](drm-import.md)期間，您可以建立自己的授權。 Windows媒體 DRM 授權可透過幾種不同的方式撰寫，但若要建立您自己的授權，您必須使用 (XMR) 二進位架構的可延伸媒體許可權。 如需詳細資訊，請參閱 [建立 XMR 授權](building-an-xmr-license.md)。

當您建立授權時，您可以藉由呼叫 [**IWMDRMLicenseManagement：： StoreLicense**](iwmdrmlicensemanagement-storelicense.md) 方法，將它新增至本機授權存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**取得授權**](acquiring-licenses.md)
</dt> <dt>

[**建立 XMR 授權**](building-an-xmr-license.md)
</dt> </dl>

 

 




