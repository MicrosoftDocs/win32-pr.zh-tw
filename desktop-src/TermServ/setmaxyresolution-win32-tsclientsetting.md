---
title: Win32_TSClientSetting 類別的 SetMaxYResolution 方法
description: 設定 MaxYResolution 屬性。
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- SetMaxYResolution 方法遠端桌面服務
- SetMaxYResolution 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetMaxYResolution 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988035"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a>Win32 TSClientSetting 類別的 SetMaxYResolution 方法 \_

設定 **MaxYResolution** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaxYResolution* \[在\]
</dt> <dd>

伺服器支援的新最大 Y 解析度。 最小值是200，而最大值是2048。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





