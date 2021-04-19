---
title: ROTFlags
description: 控制在執行中的物件資料表中，COM 伺服器的註冊 (ROT) 。
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- ROTFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967817"
---
# <a name="rotflags"></a>ROTFlags

控制在執行中的物件資料表中，COM 伺服器的註冊 (ROT) 。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 旗標值 | 常數                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>ROTREGFLAGS \_ ALLOWANYCLIENT 描述

如果 COM 伺服器想要在 ROT 中註冊，並允許任何用戶端存取註冊，則必須使用 **ROTFLAGS \_ ALLOWANYCLIENT** 旗標。 "Activate As Activator" COM 伺服器無法指定 **ROTFLAGS \_ ALLOWANYCLIENT** ，因為 DCOM 服務控制管理員 (DCOMSCM) 強制對此旗標進行詐騙檢查。 因此，在 Windows Vista 和更新版本中，COM 新增了 **ROTFlags** 登錄專案的支援，可讓伺服器規定其衰減註冊可供任何用戶端使用。

專案必須存在於 **HKEY \_ 本機 \_ 電腦** hive 中。 此專案提供「啟用為啟動程式」伺服器，其功能與 **ROTFLAGS \_ ALLOWANYCLIENT** 為 RunAs 伺服器提供的功能相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AppID 金鑰](appid-key.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




