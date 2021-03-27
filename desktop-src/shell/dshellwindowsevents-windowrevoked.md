---
description: 當 Shell 視窗的註冊撤銷時呼叫。
title: DShellWindowsEvents. WindowRevoked 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974913"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>DShellWindowsEvents. WindowRevoked 方法

當 Shell 視窗的註冊撤銷時呼叫。

## <a name="syntax"></a>語法


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*lCookie* \[在\]
</dt> <dd>

類型： **整數**

識別已撤銷之視窗的 cookie。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當某個視窗註冊為 Shell 視窗時，會授與一個 cookie。 如需詳細資訊，請參閱 [**註冊**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| 產品<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**撤銷**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




