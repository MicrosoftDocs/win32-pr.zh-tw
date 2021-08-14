---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetPriority 方法
description: 設定外掛程式的優先順序。
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority 方法遠端桌面服務
- SetPriority 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetPriority 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfe18b5998a1b8576cbd1a8f3c793e355469cfeff44f585dcb167a3b154803a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987738"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Win32 SessionDirectoryVMMPlugin 類別的 SetPriority 方法 \_

設定外掛程式的優先順序。

## <a name="syntax"></a>語法


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*優先順序* \[在\]
</dt> <dd>

外掛程式的優先順序。 值愈高，外掛程式的優先順序愈高。 優先權預設為零。

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

 

 





