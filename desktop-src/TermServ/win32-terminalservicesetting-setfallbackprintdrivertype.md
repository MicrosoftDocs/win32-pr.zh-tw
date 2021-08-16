---
title: Win32_TerminalServiceSetting 類別的 SetFallbackPrintDriverType 方法
description: SetFallbackPrintDriverType 方法會設定類別的 FallbackPrintDriverType 屬性。
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- SetFallbackPrintDriverType 方法遠端桌面服務
- SetFallbackPrintDriverType 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetFallbackPrintDriverType 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137861"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 SetFallbackPrintDriverType 方法 \_

**SetFallbackPrintDriverType** 方法會設定類別的 **FallbackPrintDriverType** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FallbackPrintDriverType* \[在\]
</dt> <dd>

設定 **FallbackPrintDriverType** 屬性，以允許或拒絕新的遠端桌面服務連接。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

無備用驅動程式。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

最佳猜測。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

最佳猜測。 如果找不到相符項，則會切換回 Hewlett-Packard 印表機控制語言 (PCL) 。

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

最佳猜測。 如果找不到相符的結果，則會改回 Postscript (PS) 。

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

最佳猜測。 如果找不到相符的，則會顯示 PS 和 PCL 驅動程式。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

