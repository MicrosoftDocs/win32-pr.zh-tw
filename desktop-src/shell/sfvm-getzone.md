---
description: 允許回呼物件提供網際網路區域資訊。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: 'SFVM_GETZONE 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946823f1081a8cc3e01c917e424e3bdd41861f85b0abe0cad654ea09c296f8fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048427"
---
# <a name="sfvm_getzone-message"></a>SFVM \_ GETZONE 訊息

\[這項通知是透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 支援。 Windows 的後續版本中可能不支援此功能。\]

允許回呼物件提供網際網路區域資訊。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*區域* \[擴展\]
</dt> <dd>

下列其中一個指出網際網路區域的值。 這些值會構成 [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) 列舉，定義于 urlmon.dll 中。

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE \_ 本機 \_ 電腦**


</dt> <dd>

使用者的本機電腦上已有內容使用的區域。 使用者介面不會公開此區域。

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE \_ 內部網路**


</dt> <dd>

用於內部網路上找到的內容的區域。

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ 信任**


</dt> <dd>

用於網際網路上受信任網站的區域。

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ 網際網路**


</dt> <dd>

網際網路上大部分內容所使用的區域。

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ 不受信任**


</dt> <dd>

不受信任的網站所使用的區域。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
