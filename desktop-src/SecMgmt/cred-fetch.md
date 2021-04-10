---
description: 定義值，決定如何提取群組受管理的服務帳戶 (gMSA) 的認證。
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: 'CRED_FETCH 列舉 (Secpkg .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944754"
---
# <a name="cred_fetch-enumeration"></a>認證 \_ 提取列舉

定義值，決定如何提取群組受管理的服務帳戶 (gMSA) 的認證。

## <a name="syntax"></a>Syntax


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**
</dt> <dd>

表示作業系統應該先嘗試從本機快取取出密碼。 如果需要取得密碼，則作業系統應聯繫網域控制站以取得密碼。 如果失敗，則會傳回狀態為 success 的任何快取密碼。

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**
</dt> <dd>

將本機 DPAPI 認證傳回給呼叫者。  (Ssp) 的 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly)通常不需要使用此列舉。

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**
</dt> <dd>

強制作業系統嘗試從網域控制站讀取密碼。 在密碼變換期間，網域控制站和其他成員主機上的密碼可能已變更，但 gMSA 成員主機會將密碼識別為有效。 這種情況可能是因為不同網域控制站之間的時鐘誤差問題所造成。 當指定這個值時，作業系統會判斷是否可能因為時鐘誤差而可能變更密碼，如果是，則會抓取密碼。 否則會傳回快取的認證。 如果沒有快取的認證，則作業系統會嘗試從網域控制站取得一個。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Secpkg。h</dt> </dl> |



 

