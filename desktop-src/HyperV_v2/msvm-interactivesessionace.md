---
description: 表示存取控制專案 (ACE) ，可判斷虛擬機器的互動式會話存取。
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967162"
---
# <a name="msvm_interactivesessionace-class"></a>Msvm \_ InteractiveSessionACE 類別

表示 *存取控制專案* (ACE) ，可判斷虛擬機器的互動式會話存取。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>成員

**Msvm \_ InteractiveSessionACE** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ InteractiveSessionACE** 類別具有這些屬性。

<dl> <dt>

**AccessType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 ACE 是否授與或拒絕受信任者的存取權。

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**允許存取** (0) 


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**拒絕存取** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**受託 人**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別 ACE 授與或拒絕存取的安全性主體。 這個屬性的有效格式包括 Windows SAM 相容的使用者名稱格式和 Windows SID 字串格式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetInteractiveSessionACL**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




