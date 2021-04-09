---
title: DefaultIcon
description: 提供 iconic 物件簡報的預設圖示資訊。
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024147"
---
# <a name="defaulticon"></a>DefaultIcon

提供 iconic 物件簡報的預設圖示資訊。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定物件應用程式之可執行檔名稱的完整路徑，以及可執行檔中圖示的資源索引。

例如，當控制項最小化至圖示時， **DefaultIcon** 會識別要使用的圖示。 此專案包含伺服器應用程式之可執行檔名稱的完整路徑，以及可執行檔中圖示的資源索引。 應用程式可以使用 **DefaultIcon** 所提供的資訊，透過 [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)取得圖示控制碼。

 

 