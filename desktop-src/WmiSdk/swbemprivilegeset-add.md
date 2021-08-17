---
description: SWbemPrivilegeSet 物件的 Add 方法會將 SWbemPrivilege 物件加入至 SWbemPrivilegeSet 集合。 如果集合中已經存在具有相同名稱的許可權，則會予以取代。
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 54b45779f4954f1cee454b5cf171e374e215555902e3389c7c47f5a59bc989eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954868"
---
# <a name="swbemprivilegesetadd-method"></a>SWbemPrivilegeSet 新增方法

[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **Add** 方法會將 [**SWbemPrivilege**](swbemprivilege.md)物件加入至 **SWbemPrivilegeSet** 集合。 如果集合中已經存在具有相同名稱的許可權，則會予以取代。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iPrivilege* 
</dt> <dd>

必要。 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)群組中的其中一個 WMI 常數。 這些常數基本上是代表特定許可權的整數。 例如，若要新增可讓您關閉電腦系統的許可權，請使用 **wbemPrivilegeShutdown** 常數。 在腳本中，您必須使用等同于 23 (0x17) 的數位。 如需這些常數和相關聯的許可權字串的完整清單，請參閱 [**許可權常數**](privilege-constants.md)。

</dd> <dt>

*bIsEnabled* \[選\]
</dt> <dd>

啟用或停用此許可權的布林值。 預設值為 **TRUE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此方法會傳回代表新許可權的 [**SWbemPrivilege**](swbemprivilege.md) 物件。 否則，會傳回 null 物件。

## <a name="error-codes"></a>錯誤碼

完成 **Add** 方法時， **Err** 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> </dl>

## <a name="examples"></a>範例

使用這個方法的程式碼範例如 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 主題中所述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet。移除**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**許可權常數**](privilege-constants.md)
</dt> </dl>

 

 




