---
description: Win32 \_ ComClassAutoEmulator 關聯 WMI 類別會建立元件物件模型 (COM) 類別和它自動模擬的另一個 com 類別之間的關聯。
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba849eed744ff342cfde10d0f31072d4e898cf52cf4e6966760f780236c56df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986378"
---
# <a name="win32_comclassautoemulator-class"></a>Win32 \_ ComClassAutoEmulator 類別

**Win32 \_ ComClassAutoEmulator** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立元件物件模型 (COM) 類別和它自動模擬的另一個 com 類別之間的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>成員

**Win32 \_ ComClassAutoEmulator** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ComClassAutoEmulator** 類別具有這些屬性。

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ ClassicCOMClass**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) 
</dt> </dl>

代表可自動模擬相關聯 COM 元件之 COM 元件的實例參考。 這項資訊是透過 AutoTreatAs 登錄專案取得。

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ ClassicCOMClass**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) 
</dt> </dl>

實例的參考，代表由另一個元件自動模擬的 COM 元件。

</dd> </dl>

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

 

