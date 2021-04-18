---
title: Win32_RDMSManagementData 類別的 SynchronizePublishingData 方法
description: 將遠端桌面管理服務的指定發佈資料集同步處理 (RDMS) 。
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- SynchronizePublishingData 方法遠端桌面服務
- SynchronizePublishingData 方法遠端桌面服務，Win32_RDMSManagementData 類別
- Win32_RDMSManagementData 類別遠端桌面服務，SynchronizePublishingData 方法
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384557"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Win32 RDMSManagementData 類別的 SynchronizePublishingData 方法 \_

將遠端桌面管理服務的指定發佈資料集同步處理 (RDMS) 。

## <a name="syntax"></a>語法


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*內容* \[在\]
</dt> <dd>

要同步處理之發行資料的內容資訊。

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

[**Win32 \_ RDMSManagementData**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





