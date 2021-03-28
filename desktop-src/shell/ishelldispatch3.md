---
description: 擴充 IShellDispatch2 物件。
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: 'IShellDispatch3 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972376"
---
# <a name="ishelldispatch3-object"></a>IShellDispatch3 物件

擴充 [**IShellDispatch2**](ishelldispatch2-object.md) 物件。 除了 **IShellDispatch2** 支援的屬性和方法之外， **IShellDispatch3** 還支援一個新的方法。

> [!Note]  
> **IShellDispatch3** 是透過 [**Shell**](shell.md) 物件來執行和存取。

 

## <a name="members"></a>成員

**IShellDispatch3** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IShellDispatch3** 物件有這些方法。



| 方法                                             | 描述                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | 將檔案加入最近使用的 (MRU) 清單中。<br/> |



 

## <a name="remarks"></a>備註

如需 Windows 服務的討論，請參閱 [服務](../services/services.md) 檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell 物件**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> </dl>

 

 
