---
description: 當視窗註冊為 Shell 視窗時呼叫。
title: DShellWindowsEvents. WindowRegistered 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 7ad7270f9054b875eabcb1fd9f5a7ab2e299a5916d55ef4630988921b6b2f4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455568"
---
# <a name="dshellwindowseventswindowregistered-method"></a>DShellWindowsEvents. WindowRegistered 方法

當視窗註冊為 Shell 視窗時呼叫。

## <a name="syntax"></a>語法


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*lCookie* \[在\]
</dt> <dd>

類型： **整數**

識別已註冊之視窗的 cookie。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當某個視窗註冊為 Shell 視窗時，會授與一個 cookie。 如需詳細資訊，請參閱 [**註冊**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Product<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRevoked**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**註冊**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**RegisterPending**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




