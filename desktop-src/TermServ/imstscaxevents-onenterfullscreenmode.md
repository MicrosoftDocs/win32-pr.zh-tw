---
title: IMsTscAxEvents OnEnterFullScreenMode 方法
description: 當用戶端進入全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式快速鍵組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- OnEnterFullScreenMode 方法遠端桌面服務
- OnEnterFullScreenMode 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnEnterFullScreenMode 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e40da93f0e29fb183cea540b0f195d61c4969d65c2b7829bf86d8e3c8eba81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512398"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a>IMsTscAxEvents：： OnEnterFullScreenMode 方法

當用戶端進入全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。

## <a name="syntax"></a>語法


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





