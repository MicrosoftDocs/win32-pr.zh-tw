---
title: Win32_RDMSCollectionProperties 類別的 GetProvisioningProperties 方法
description: 抓取虛擬桌面集合的布建屬性。
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- GetProvisioningProperties 方法遠端桌面服務
- GetProvisioningProperties 方法遠端桌面服務，Win32_RDMSCollectionProperties 類別
- Win32_RDMSCollectionProperties 類別遠端桌面服務，GetProvisioningProperties 方法
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd97ca6f3ec79320509881d79bc0ea24d73944a0ae3634d331073517c8bc0fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130443"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Win32 RDMSCollectionProperties 類別的 GetProvisioningProperties 方法 \_

抓取虛擬桌面集合的布建屬性。

## <a name="syntax"></a>語法


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PoolVhdType* \[擴展\]
</dt> <dd>

在集合中指定虛擬機器集區 (虛擬硬碟) 格式的 VHD。

<dt>

複製
</dt> <dd>

複製的 VHD。

</dd> <dt>

DiffDisk
</dt> <dd>

差異 VHD。

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[擴展\]
</dt> <dd>

接收主要 VM 映射的路徑。

</dd> <dt>

*NamePrefix* \[擴展\]
</dt> <dd>

接收要附加至虛擬機器名稱開頭的名稱前置詞。

</dd> <dt>

*NameStartIndex* \[擴展\]
</dt> <dd>

開始索引。

</dd> <dt>

*LocalVmLocation* \[擴展\]
</dt> <dd>

接收 Hyper-v 伺服器上虛擬機器的本機路徑。 如果此參數設定為 **Null** 或為空白，則會使用預設的虛擬機器目錄。

</dd> <dt>

*LocalGoldVmLocation* \[擴展\]
</dt> <dd>

當 *PoolVhdTpe* 參數設定為 "DiffDisk" 時，接收黃金 VHD 映射的本機路徑。 如果此參數設定為 **Null** 或為空白，則會使用預設的虛擬機器目錄。

</dd> <dt>

*RunFromSMB* \[擴展\]
</dt> <dd>

接收值，指出是否要從伺服器訊息區 (SMB) 共用執行集合。 **TRUE** 表示從 SBM 共用執行虛擬機器;相反 **FALSE**。

</dd> <dt>

*SMBLocation* \[擴展\]
</dt> <dd>

如果已啟用 SMB 共用，則會接收 SMB 共用的路徑。

</dd> <dt>

*SMBStreaming* \[擴展\]
</dt> <dd>

接收值，指出是否已啟用 SMB 串流。 如果已啟用 SMB 共用，則 **為 TRUE** ;相反 **FALSE**。

</dd> <dt>

*VmDomain* \[擴展\]
</dt> <dd>

接收集合中虛擬機器的功能變數名稱。

</dd> <dt>

*VmOU* \[擴展\]
</dt> <dd>

接收集合中虛擬機器的 Active Directory 組織單位 (OU) 。

</dd> <dt>

*ProductKey* \[擴展\]
</dt> <dd>

接收集合中虛擬機器的作業系統產品金鑰。

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

[**Win32 \_ RDMSCollectionProperties**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





