---
description: Win32 \_ DiskDriveToDiskPartition 關聯 WMI 類別會關聯磁片磁碟機和其上現有的磁碟分割。
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c92e9cc8a71516fa105e350ae8070ca417024c1802e9ea8a676d7355cb3aea7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675091"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>Win32 \_ DiskDriveToDiskPartition 類別

**Win32 \_ DiskDriveToDiskPartition** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯磁片磁碟機和其上現有的磁碟分割。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ DiskDriveToDiskPartition** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ DiskDriveToDiskPartition** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ DiskDrive**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DiskDrive" ) 
</dt> </dl>

此實例的參考，代表磁碟分割所在之磁片磁碟機的屬性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ DiskPartition**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 DiskPartition」 \_ ) 
</dt> </dl>

代表位於磁片磁碟機上的磁碟分割之實例的參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ DiskDriveToDiskPartition** 類別衍生自 [**CIM \_ MediaPresent**](cim-mediapresent.md)。

如需如何使用這個類別的討論，請參閱 [使用 PowerShell 對應磁片磁碟機和磁碟分割](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) ，以及 [如何將邏輯磁碟機和實體磁片相互關聯？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog 文章。

## <a name="examples"></a>範例

[使用 Powershell 收集磁片/磁碟分割/掛接點資訊](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0)powershell 範例會使用 **Win32 \_ DiskDriveToDiskPartition** 來傳回本機磁片/磁碟分割和掛接點的相關資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI 工作：磁片和檔案系統](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

