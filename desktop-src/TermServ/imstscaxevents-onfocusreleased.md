---
title: IMsTscAxEvents OnFocusReleased 方法
description: 在按下放開焦點按鍵組合時呼叫。 例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- OnFocusReleased 方法遠端桌面服務
- OnFocusReleased 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnFocusReleased 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673916c3a538f21ceea5b0b7578bb9e8f225ec2a349e38015eab0b50d73935aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512338"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>IMsTscAxEvents：： OnFocusReleased 方法

在按下放開焦點按鍵組合時呼叫。 例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。

此事件可讓 ActiveX 控制容器離開 ActiveX 控制項的控制權。 例如，這在您沒有滑鼠的情況下很有用，而像 ALT + TAB 等特殊按鍵組合會重新導向至伺服器。 在此情況下，您沒有辦法將鍵盤焦點傳回本機桌面。 不過，使用 ctrl + alt + 向左鍵或 ctrl + alt + 向右鍵組合時，ActiveX 容器可以接聽此事件，並將焦點離開 ActiveX 控制項來回應。

## <a name="syntax"></a>語法


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iDirection* \[在\]
</dt> <dd>

1 (CTRL + ALT + 向右鍵的方向參數) 或 1 (CTRL + ALT + 向左鍵) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當用戶端上使用遠端桌面連線6.0 時，就可以使用此事件。

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

 

 





