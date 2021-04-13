---
title: 'IRDVTaskPluginNotifySink OnTerminated 方法 (Sbtsv .h) '
description: 由工作代理程式呼叫，以要求關閉工作代理程式。
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- OnTerminated 方法遠端桌面服務
- OnTerminated 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，OnTerminated 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509347"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>IRDVTaskPluginNotifySink：： OnTerminated 方法

由工作代理程式呼叫，以要求關閉工作代理程式。

## <a name="syntax"></a>語法


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hr* \[在\]
</dt> <dd>

指出關機是否因為正常關機或失敗。 如果關機正常，則會包含 **\_ [確定]**。 否則，它會包含 **HRESULT** 錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Sbtsv。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





