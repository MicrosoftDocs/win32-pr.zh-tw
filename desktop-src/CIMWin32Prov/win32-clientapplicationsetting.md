---
description: Win32 \_ ClientApplicationSetting 關聯 WMI 類別會將可執行檔和元件物件模型關聯 (com) 應用程式，其中包含可執行檔的 COM 設定選項。
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 359478d7cf6069e17ae02358f4ea48ffc44169f6822f4f8b3e33dad332fab020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546368"
---
# <a name="win32_clientapplicationsetting-class"></a>Win32 \_ ClientApplicationSetting 類別

**Win32 \_ ClientApplicationSetting** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將可執行檔和元件物件模型關聯 (com) 應用程式，其中包含可執行檔的 COM 設定選項。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>成員

**Win32 \_ ClientApplicationSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ClientApplicationSetting** 類別具有這些屬性。

<dl> <dt>

**應用程式**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ DCOMApplication**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DCOMApplication" ) 
</dt> </dl>

代表 COM 應用程式之實例的參考，其中包含可執行檔的設定選項。

</dd> <dt>

**用戶端**
</dt> <dd> <dl> <dt>

資料類型： **CIM 資料 \_ 檔**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim \_ 資料檔案」 ) 
</dt> </dl>

代表使用 COM 設定之可執行檔的實例參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ClientApplicationSetting** 不支援列舉。

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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

