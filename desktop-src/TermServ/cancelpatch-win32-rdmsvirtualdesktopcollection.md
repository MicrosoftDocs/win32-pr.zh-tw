---
title: Win32_RDMSVirtualDesktopCollection 類別的 CancelPatch 方法
description: 取消虛擬機器集合中虛擬機器的軟體更新布建作業。
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- CancelPatch 方法遠端桌面服務
- CancelPatch 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，CancelPatch 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56f33a819da976187fba823ac30fada9ff38730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967320"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 CancelPatch 方法 \_

取消虛擬機器集合中虛擬機器的軟體更新布建作業。

## <a name="syntax"></a>語法


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 





