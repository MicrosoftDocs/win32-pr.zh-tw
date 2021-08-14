---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningEnumerateJobs 方法
description: 列舉此服務的虛擬桌面布建作業。
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- ProvisioningEnumerateJobs 方法遠端桌面服務
- ProvisioningEnumerateJobs 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，ProvisioningEnumerateJobs 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350220"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningEnumerateJobs 方法 \_

列舉此服務的虛擬桌面布建作業。

## <a name="syntax"></a>語法


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*JobType* \[在\]
</dt> <dd>

整數，指定要列舉的作業類型。

這個參數可以設定為下列其中一個值：

<dt>

0
</dt> <dd>

正在執行工作

</dd> <dt>

1
</dt> <dd>

已完成的工作

</dd> </dl> </dd> <dt>

*CollectionAlias* \[在\]
</dt> <dd>

要列舉之虛擬桌面集合的別名。 此參數的預設值為 FALSE，這會指定要列舉所有正在執行的作業。

</dd> <dt>

*JobGuids* \[擴展\]
</dt> <dd>

陣列，其中包含要列舉之布建作業的 **guid** 。

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

 

 





