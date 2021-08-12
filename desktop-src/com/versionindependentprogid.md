---
title: VersionIndependentProgID
description: 將 ProgID 與 CLSID 產生關聯。 此值可用來判斷物件應用程式的最新版本。
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549714"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

將 ProgID 與 CLSID 產生關聯。 此值可用來判斷物件應用程式的最新版本。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定最新版的物件應用程式。

與版本無關的 ProgID 只會由應用程式程式碼儲存和維護。 當指定與版本無關的 ProgID 時， [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 函數會傳回目前版本的 CLSID。

您可以使用 [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) ，在這兩種標記法之間進行轉換。

 

 




