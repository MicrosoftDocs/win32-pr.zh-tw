---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningJobGetReport 方法
description: 取得虛擬桌面布建作業狀態的相關報告。
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- ProvisioningJobGetReport 方法遠端桌面服務
- ProvisioningJobGetReport 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，ProvisioningJobGetReport 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999608"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningJobGetReport 方法 \_

取得虛擬桌面布建作業狀態的相關報告。

## <a name="syntax"></a>語法


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*JobGuid* \[在\]
</dt> <dd>

可唯一識別布建作業的 **GUID** 。

</dd> <dt>

*JobReportXml* \[擴展\]
</dt> <dd>

字串，包含 XML 格式的報表。

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

 

 





