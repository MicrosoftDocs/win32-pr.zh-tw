---
description: SWbemPrivilegeSet 物件的 DeleteAll 方法會移除集合中的擁有權限，因此將它清空。
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet. DeleteAll 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985318"
---
# <a name="swbemprivilegesetdeleteall-method"></a>SWbemPrivilegeSet. DeleteAll 方法

[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **DeleteAll** 方法會移除集合中的擁有權限，因此將它清空。

## <a name="syntax"></a>語法


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

**DeleteAll** 方法完成後， **Err** 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet。移除**](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




