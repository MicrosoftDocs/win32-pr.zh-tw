---
description: 結束工作完成。
ms.assetid: C64C57E3-593C-47AE-A005-F468E7C588EF
title: TaskCompletionClient：： RevokeTaskCompletion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.RevokeTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 2b0130ae2e90c2f592c158fb0730461eab8a78b192ae81f7cc7aaa4139c83483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773658"
---
# <a name="taskcompletionclientrevoketaskcompletion-method"></a>TaskCompletionClient：： RevokeTaskCompletion 方法

結束工作完成。

## <a name="syntax"></a>語法


```C++
HRESULT RevokeTaskCompletion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




