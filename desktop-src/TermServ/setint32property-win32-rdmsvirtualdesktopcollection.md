---
title: Win32_RDMSVirtualDesktopCollection 類別的 SetInt32Property 方法
description: 更新虛擬桌面集合的整數屬性。
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- SetInt32Property 方法遠端桌面服務
- SetInt32Property 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，SetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105845"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 SetInt32Property 方法 \_

更新虛擬桌面集合的整數屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

識別要更新之屬性的索引鍵。

</dd> <dt>

*值* \[在\]
</dt> <dd>

新的屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





