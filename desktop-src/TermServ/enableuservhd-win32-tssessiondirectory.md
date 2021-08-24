---
title: Win32_TSSessionDirectory 類別的 EnableUserVhd 方法
description: 在 RDSH 伺服器上啟用使用者設定檔 VHD。
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- EnableUserVhd 方法遠端桌面服務
- EnableUserVhd 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，EnableUserVhd 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871738"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Win32 TSSessionDirectory 類別的 EnableUserVhd 方法 \_

在 RDSH 伺服器上啟用使用者設定檔 VHD。

## <a name="syntax"></a>語法


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UvhdShareUrl* \[在\]
</dt> <dd>

儲存所有使用者設定檔 Vhd 之共用的位置。

</dd> <dt>

*UvhdRoamingPolicyXml* \[在\]
</dt> <dd>

使用者設定檔 VHD 的漫遊原則。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





