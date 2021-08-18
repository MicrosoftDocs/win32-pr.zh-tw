---
description: 接收 IShellWindows 視窗註冊事件。
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: 'DShellWindowsEvents 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 13335268b892e4ac95520221fcd2e413c9c255225ccd8fc36c3c73cbf8c327a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009538"
---
# <a name="dshellwindowsevents-object"></a>DShellWindowsEvents 物件

接收 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) 視窗註冊事件。

## <a name="members"></a>成員

**DShellWindowsEvents** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**DShellWindowsEvents** 物件有這些方法。



| 方法                                                           | 描述                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | 當視窗註冊為 Shell 視窗時呼叫。 <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | 當 Shell 視窗的註冊撤銷時呼叫。 <br/> |



 

## <a name="remarks"></a>備註

使用 **DShellWindowsEvents** 來監視如何註冊或撤銷 Shell 視窗。 如需詳細資訊，請參閱 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| 產品<br/> | Internet Explorer 5<br/>                                                                                           |
| 標頭<br/>  | <dl> <dt>Exdisp。h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




