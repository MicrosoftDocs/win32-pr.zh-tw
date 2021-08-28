---
title: LoadUserSettings
description: 判斷 COM 是否會載入執行的 COM 伺服器的使用者設定檔，做為啟動使用者應用程式識別。
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- LoadUserSettings 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731038"
---
# <a name="loadusersettings"></a>LoadUserSettings

判斷 COM 是否會載入執行的 COM 伺服器的使用者設定檔，做為啟動使用者應用程式識別。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。 如果 *值* 為非零值，則 com 會載入用來啟動 COM 伺服器之使用者帳戶的設定檔。 如果 *值* 為零或不存在，com 將不會載入用來啟動 COM 伺服器之使用者帳戶的設定檔。

如果有 [**RunAs**](runas.md) 專案存在，就會忽略此設定。

 

 




