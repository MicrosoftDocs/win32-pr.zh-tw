---
description: 可變動字串緩衝區的控制碼，可供您用來建立 HSTRING。
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: 'HSTRING_BUFFER (Hstring) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f115ca18b4bf5b81bbd7004259aa525517c05a3adc0f6376f7d16df3e3ce679
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733818"
---
# <a name="hstring_buffer"></a>HSTRING \_ 緩衝區

可變動字串緩衝區的控制碼，可供您用來建立 [**HSTRING**](hstring.md)。


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>備註

**HSTRING \_BUFFER** 表示字串緩衝區，您可以在將其轉換為不可變的 [**HSTRING**](hstring.md)之前加以修改。

呼叫 [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) 函數來建立 **HSTRING \_ 緩衝區**。 呼叫 [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) ，將 **HSTRING \_ 緩衝區** 轉換成不可變的 [**HSTRING**](hstring.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Hstring。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
