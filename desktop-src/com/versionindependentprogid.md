---
title: VersionIndependentProgID
description: 將 ProgID 與 CLSID 產生關聯。 此值可用來判斷物件應用程式的最新版本。
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022095"
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

 

 




