---
title: 'Win32_TSVirtualIP 類別的 RemoveProgram 方法 (Bdaiface) '
description: 從使用 IP 虛擬化的程式清單中移除程式。
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- RemoveProgram 方法遠端桌面服務
- RemoveProgram 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，RemoveProgram 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44d955c7547a308086ea365681a5991012fe65e390ebe296f031f0c0ef99856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058616"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Win32 TSVirtualIP 類別的 RemoveProgram 方法 \_

從使用 IP 虛擬化的程式清單中移除程式。

## <a name="syntax"></a>語法


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProgramPath* \[在\]
</dt> <dd>

類型： **字串**

要從清單中移除之程式的路徑和檔案名。 如果找不到程式，則會傳回錯誤。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Bdaiface。h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





