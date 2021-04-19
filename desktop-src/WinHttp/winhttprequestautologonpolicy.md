---
description: 包含自動登入原則的可能設定。
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: WinHttpRequestAutoLogonPolicy 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974039"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>WinHttpRequestAutoLogonPolicy 列舉

**WinHttpRequestAutoLogonPolicy** 列舉包含 [自動登入原則](authentication-in-winhttp.md)的可能設定。

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**\_一律 AutoLogonPolicy**
</dt> <dd>

系統會針對所有要求執行使用預設認證的已驗證登入。

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**
</dt> <dd>

使用預設認證的已驗證登入，只會針對近端內部網路上的要求執行。 在目前的 proxy 設定中，近端內部網路會被視為 proxy 略過清單上的任何伺服器。

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ 永不**
</dt> <dd>

不會自動使用驗證。

</dd> </dl>

## <a name="remarks"></a>備註

若要設定自動登入原則，請呼叫 [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) 方法，並指定上述其中一個常數。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




