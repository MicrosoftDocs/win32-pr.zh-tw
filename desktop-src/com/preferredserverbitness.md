---
title: PreferredServerBitness
description: 設定此 COM 伺服器的慣用架構（32位或64位）。
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- PreferredServerBitness 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316546"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

設定此 COM 伺服器的慣用架構（32位或64位）。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>備註

這是只能在64位版本的 Windows 上使用的 **REG \_ DWORD** 值。



| 值 | 描述                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 將伺服器架構與用戶端架構比對。 例如，如果用戶端是32位，請使用32位版本的伺服器（如果有的話）。 如果沒有，用戶端的啟用要求將會失敗。 |
| 2     | 使用32位版本的伺服器。 如果不存在，用戶端的啟用要求將會失敗。                                                                                                      |
| 3     | 使用64位版本的伺服器。 如果不存在，用戶端的啟用要求將會失敗。                                                                                                      |



 

如果此值不存在，則：

-   如果裝載伺服器的電腦執行的是 Windows XP 或 Windows Server 2003 （未安裝 SP1 或更新版本），則 COM 會偏好使用64位版本的伺服器（如果有的話）：否則，它會啟用32位版本的伺服器。
-   如果裝載伺服器的電腦執行的是 Windows Server 2003 SP1 或更新版本，則 COM 會嘗試將伺服器架構與用戶端架構比對。 換句話說，對於32位用戶端，COM 會啟用32位伺服器（如果有的話）。否則，它會啟用64位版本的伺服器。 若為64位用戶端，COM 會啟用64位伺服器（如果有的話）。否則會啟動32位伺服器。

用戶端也可以透過 CLSCTX \_ activate \_ 32 \_ 位 \_ 伺服器和 CLSCTX activate 64 bit 伺服器旗標來指定自己的架構喜好設定 \_ \_ \_ \_ ，這些將覆寫伺服器的喜好設定。 如需詳細資訊，以及用戶端與伺服器架構喜好設定之間可能互動的圖表，請參閱 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 