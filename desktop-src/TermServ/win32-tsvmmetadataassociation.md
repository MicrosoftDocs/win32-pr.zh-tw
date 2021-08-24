---
title: Win32_TSVmMetadataAssociation 類別
description: 代表遠端桌面虛擬機器與其中繼資料屬性之間的關聯。
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation 類別遠端桌面服務
- Win32_TSVmMetadataAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe3389bb03c9e3f33a2cc3e33450318b68171f7ac35fffeaaa3976cb5ae3a33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419998"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Win32 \_ TSVmMetadataAssociation 類別

代表遠端桌面虛擬機器與其中繼資料屬性之間的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>成員

**Win32 \_ TSVmMetadataAssociation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSVmMetadataAssociation** 類別具有這些屬性。

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

資料類型： **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)類別的實例，表示虛擬機器的中繼資料。

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

資料類型： **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

代表虛擬機器之 [**Win32 \_ TSVm**](win32-tsvm.md) 類別的實例。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

