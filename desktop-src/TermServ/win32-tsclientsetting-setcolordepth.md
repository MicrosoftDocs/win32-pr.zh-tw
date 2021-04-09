---
title: Win32_TSClientSetting 類別的 SetColorDepth 方法
description: SetColorDepth 方法會設定類別的 ColorDepth 屬性。
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- SetColorDepth 方法遠端桌面服務
- SetColorDepth 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetColorDepth 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934963"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Win32 TSClientSetting 類別的 SetColorDepth 方法 \_

**SetColorDepth** 方法會設定類別的 **ColorDepth** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ColorDepth* \[在\]
</dt> <dd>

**ColorDepth** 屬性的新值。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

每圖元8位

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

每圖元15個位

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

每圖元16個位

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

每圖元24個位

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**.5**


</dt> <dd>

每圖元32位

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

