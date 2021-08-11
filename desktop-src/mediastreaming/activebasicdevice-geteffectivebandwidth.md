---
title: 'ActiveBasicDevice GetEffectiveBandwidth 方法 (PlayToDevice .h) '
description: 取得裝置目前有效的頻寬。
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- GetEffectiveBandwidth 方法媒體串流 API
- GetEffectiveBandwidth 方法媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，GetEffectiveBandwidth 方法
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236780"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>ActiveBasicDevice：： GetEffectiveBandwidth 方法

取得裝置目前有效的頻寬。

## <a name="syntax"></a>語法


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*transmitSpeed* \[在中，retval\]
</dt> <dd>

指定是否抓取傳送速率或抓取接收速度。

**true** 表示取得傳送速率。 **false** 表示取得接收速度。

</dd> <dt>

*currentSpeed* \[擴展\]
</dt> <dd>

接收目前有效的頻寬。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

