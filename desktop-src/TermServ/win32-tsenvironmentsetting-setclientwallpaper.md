---
title: Win32_TSEnvironmentSetting 類別的 SetClientWallPaper 方法
description: SetClientWallPaper 方法會設定 ClientWallPaper 屬性。
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- SetClientWallPaper 方法遠端桌面服務
- SetClientWallPaper 方法遠端桌面服務，Win32_TSEnvironmentSetting 類別
- Win32_TSEnvironmentSetting 類別遠端桌面服務，SetClientWallPaper 方法
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685847"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Win32 TSEnvironmentSetting 類別的 SetClientWallPaper 方法 \_

**SetClientWallPaper** 方法會設定 **ClientWallPaper** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientWallPaper* \[在\]
</dt> <dd>

旗標停用或啟用 **ClientWallPaper** 屬性，指定用戶端上是否顯示背景 (或壁紙) 影像。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

用戶端上不會顯示背景 (或壁紙) 影像。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

背景 (或壁紙) 影像會顯示在用戶端上。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

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

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

