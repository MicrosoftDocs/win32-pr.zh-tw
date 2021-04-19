---
description: 通知系統應用程式已儲存其資料，並已準備好暫停。
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'ISuspendingDeferral：： Complete 方法 (ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970608"
---
# <a name="isuspendingdeferralcomplete-method"></a>ISuspendingDeferral：： Complete 方法

通知系統應用程式已儲存其資料，並已準備好暫停。

## <a name="syntax"></a>語法


```C++
HRESULT Complete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 標頭<br/>                   | <dl> <dt>ApplicationModel。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 




