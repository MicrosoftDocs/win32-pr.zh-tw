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
ms.openlocfilehash: 8f02095415ff2682e1f2a2eeb21c4afe0754b72251f6129856f1b6a415913cf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720914"
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

如需 Windows 服務的討論，請參閱[服務](../services/services.md)檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
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

 

 
