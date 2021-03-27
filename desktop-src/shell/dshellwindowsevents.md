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
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974880"
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

 

 




