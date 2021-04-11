---
description: SWbemPrivilege 物件代表單一許可權。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: 'SWbemPrivilege 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027480"
---
# <a name="swbemprivilege-object"></a>SWbemPrivilege 物件

**SWbemPrivilege** 物件代表單一許可權。 VBScript **CreateObject** 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemPrivilege** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SWbemPrivilege** 物件具有這些屬性。



| 屬性                                                     | 存取類型           | Description                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**Displayname**](swbemprivilege-displayname.md)<br/> | 唯讀<br/>  | 此許可權的顯示名稱。<br/>                                       |
| [**識別碼**](swbemprivilege-identifier.md)<br/>   | 讀取/寫入<br/> | 表示正在設定或抓取之許可權的整數。<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | 讀取/寫入<br/> | 指出是否已啟用此許可權的布林值。<br/>            |
| [**Name**](swbemprivilege-name.md)<br/>               | 唯讀<br/>  | 此許可權的名稱。<br/>                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemPrivilege<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




