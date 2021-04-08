---
title: Win32_RDMSManagementData 類別的 SynchronizeAllPublishingData 方法
description: 同步處理遠端桌面管理服務 (RDMS) 的所有發佈資料。
ms.assetid: 3a2135c3-26d6-4b6e-9680-f2d07f33ec05
ms.tgt_platform: multiple
keywords:
- SynchronizeAllPublishingData 方法遠端桌面服務
- SynchronizeAllPublishingData 方法遠端桌面服務，Win32_RDMSManagementData 類別
- Win32_RDMSManagementData 類別遠端桌面服務，SynchronizeAllPublishingData 方法
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizeAllPublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4db541954e1595c7b2fc8340f05a9415ad39b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685852"
---
# <a name="synchronizeallpublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Win32 RDMSManagementData 類別的 SynchronizeAllPublishingData 方法 \_

同步處理遠端桌面管理服務 (RDMS) 的所有發佈資料。

## <a name="syntax"></a>語法


```mof
uint32 SynchronizeAllPublishingData();
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

[**Win32 \_ RDMSManagementData**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





