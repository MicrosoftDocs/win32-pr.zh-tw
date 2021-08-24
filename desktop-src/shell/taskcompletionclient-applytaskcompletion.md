---
description: 開始工作完成。
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: TaskCompletionClient：： ApplyTaskCompletion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 58c95144077697f1655547a58571ce3475355aa96040ce1815bd3178bc9a1290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773668"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>TaskCompletionClient：： ApplyTaskCompletion 方法

開始工作完成。

## <a name="syntax"></a>語法


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptcfCategory* 
</dt> <dd>

指出工作類別的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

唯一支援的 *ptcfCategory* 值為0x08000000。

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

 

 




