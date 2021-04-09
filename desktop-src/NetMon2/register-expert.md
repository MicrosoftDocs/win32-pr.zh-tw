---
description: 專家必須實行註冊專家功能。 網路監視器會呼叫註冊專家功能來取得專家的相關資訊。
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: '將專家回呼函式註冊 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848763"
---
# <a name="register-expert-callback-function"></a>註冊專家回呼函數

專家必須實行 **註冊** 專家功能。 網路監視器會呼叫 **註冊** 專家功能來取得專家的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pExpertInfo* \[in、out\]
</dt> <dd>

網路監視器配置之 [**EXPERTENUMINFO**](expertenuminfo.md) 結構的指標。 專家會以所有要求的資訊填入結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **TRUE**，而且函數會傳回要求的資訊。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

[**EXPERTENUMINFO**](expertenuminfo.md)結構的 **版本** 成員必須為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




