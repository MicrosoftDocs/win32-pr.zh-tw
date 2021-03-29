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
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991706"
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
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




