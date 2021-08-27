---
title: Win32_SessionDirectoryVMMPlugin 類別的 GetCurrentVMMPlugin 方法
description: 取得已啟用的最高優先順序外掛程式。
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- GetCurrentVMMPlugin 方法遠端桌面服務
- GetCurrentVMMPlugin 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，GetCurrentVMMPlugin 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080108"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Win32 SessionDirectoryVMMPlugin 類別的 GetCurrentVMMPlugin 方法 \_

取得已啟用的最高優先順序外掛程式。

## <a name="syntax"></a>語法


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sName* \[擴展\]
</dt> <dd>

外掛程式的名稱。

</dd> <dt>

*sProvider* \[擴展\]
</dt> <dd>

外掛程式提供者的名稱。

</dd> <dt>

*sServiceLocation* \[擴展\]
</dt> <dd>

外掛程式應聯絡的服務位置。

</dd> <dt>

*sClassID* \[擴展\]
</dt> <dd>

外掛程式的類別識別碼。

</dd> <dt>

*優先順序* \[擴展\]
</dt> <dd>

外掛程式的優先順序。 值愈高，外掛程式的優先順序愈高。

</dd> <dt>

*已啟用* \[擴展\]
</dt> <dd>

指出外掛程式是否已啟用或停用。 如果外掛程式已啟用則 **為 True** ，否則為 **false** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





