---
title: IMsTscAxEvents OnFatalError 方法
description: 當用戶端控制項遇到嚴重錯誤時呼叫。
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- OnFatalError 方法遠端桌面服務
- OnFatalError 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnFatalError 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843848"
---
# <a name="imstscaxeventsonfatalerror-method"></a>IMsTscAxEvents：： OnFatalError 方法

當用戶端控制項遇到嚴重錯誤時呼叫。

## <a name="syntax"></a>語法


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*errorCode* \[在\]
</dt> <dd>

指示錯誤碼。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

發生未知的錯誤。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

內部錯誤碼1。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

發生記憶體不足的錯誤。

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

發生視窗建立錯誤。

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

內部錯誤代碼2。

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**.5**


</dt> <dd>

內部錯誤代碼3。 這不是有效的狀態。

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6**


</dt> <dd>

內部錯誤代碼4。

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**型**


</dt> <dd>

用戶端連接時發生無法復原的錯誤。

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Winsock 初始化錯誤。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

為了回應此事件，容器會顯示錯誤訊息並關閉。

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

 

 





