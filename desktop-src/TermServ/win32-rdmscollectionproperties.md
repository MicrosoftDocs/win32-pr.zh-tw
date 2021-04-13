---
title: Win32_RDMSCollectionProperties 類別
description: 管理虛擬桌面集合的屬性。
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties 類別遠端桌面服務
- Win32_RDMSCollectionProperties 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384449"
---
# <a name="win32_rdmscollectionproperties-class"></a>Win32 \_ RDMSCollectionProperties 類別

管理虛擬桌面集合的屬性。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSCollectionProperties** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](/windows)

### <a name="methods"></a>方法

**Win32 \_ RDMSCollectionProperties** 類別具有這些方法。



| 方法                                                                                        | 描述                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetProvisioningProperties**](getprovisioningproperties-win32-rdmscollectionproperties.md) | 抓取虛擬桌面集合的布建屬性。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ RDMSCollectionProperties** 類別具有這些屬性。

<dl> <dt>

**別名**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得集合的別名。

</dd> <dt>

**ReferenceVirtualDesktopAdapters**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的虛擬網路介面卡名稱。

</dd> <dt>

**ReferenceVirtualDesktopArchitecture**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的處理器架構。

</dd> <dt>

**ReferenceVirtualDesktopGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的 GUID。

</dd> <dt>

**ReferenceVirtualDesktopHost**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的主機伺服器名稱。

</dd> <dt>

**ReferenceVirtualDesktopMachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的電腦名稱稱。

</dd> <dt>

**ReferenceVirtualDesktopName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的名稱。

</dd> <dt>

**ReferenceVirtualDesktopOsversion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的 OS 版本。

</dd> <dt>

**ReferenceVirtualDesktopRamsizeMB**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定主要 VM 的記憶體大小。

</dd> <dt>

**ReferenceVirtualDesktopRemoteFX**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出是否已為主要 VM 啟用 RemoteFX。 如果已啟用 RemoteFX，則 **為 TRUE** ;否則 **為 FALSE**。 這個屬性的預設值為 **FALSE**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> </dl>

 

