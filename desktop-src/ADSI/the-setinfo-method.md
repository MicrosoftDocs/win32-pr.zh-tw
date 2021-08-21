---
title: SetInfo 方法
description: IADs SetInfo 方法會將這個 Active Directory 物件之屬性的目前值，從屬性快取儲存到基礎目錄存放區。 這類似于將緩衝區排清到磁片。
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- 使用 SetInfo ADSI
- 屬性 ADSI，儲存屬性的目前值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023136"
---
# <a name="the-setinfo-method"></a>SetInfo 方法

[**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)方法會將這個 Active Directory 物件之屬性的目前值，從屬性快取儲存到基礎目錄存放區。 這類似于將緩衝區排清到磁片。

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 會更新目錄中已存在的物件，或為新建立的物件建立新的目錄專案。

在 [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 呼叫時，如果已使用 [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) 控制項程式碼（例如 ADS 屬性更新或 ads 屬性）來撰寫任何屬性快取值，則 \_ 會將 \_ \_ \_ 適當的要求傳遞至基礎目錄服務。

 

 




