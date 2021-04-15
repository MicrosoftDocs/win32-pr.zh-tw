---
description: 識別 WLDP 呼叫端的主機類型。
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: 'WLDP_HOST_ID 列舉 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510392"
---
# <a name="wldp_host_id-enumeration"></a>WLDP \_ 主機 \_ 識別碼列舉

識別 WLDP 呼叫端的主機類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_主機 \_ 識別碼 \_ 不明** 
</dt> <dd>

主機類型未知。

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_主機 \_ 識別碼 \_ 全域**
</dt> <dd>

主機類型為全域原則。

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ 主機 \_ 識別碼 \_ VBA**
</dt> <dd>

主機類型為 VBScript。

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_主機 \_ 識別碼 \_ WSH**
</dt> <dd>

主機類型為 Windows Script Host。

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_主機 \_ 識別碼 \_ POWERSHELL**
</dt> <dd>

主機類型為 Windows Powershell。

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_主機 \_ 識別碼 \_ IE**
</dt> <dd>

主機類型為 Internet Explorer。

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_主機 \_ 識別碼 \_ MSI**
</dt> <dd>

主機類型為 Microsoft Windows Installer。

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_主機 \_ 識別碼 \_ 最大值** 
</dt> <dd>

最大的列舉值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl> |



 

 




