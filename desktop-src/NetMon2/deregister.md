---
description: 取消註冊匯出函數會釋出用來建立通訊協定屬性資料庫的資源。 剖析器 DLL 必須執行取消註冊。
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: '取消註冊回呼函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192633"
---
# <a name="deregister-callback-function"></a>取消註冊回呼函數

取消 **註冊** 匯出函數會釋出用來建立通訊協定 [*屬性資料庫*](p.md)的資源。 剖析器 DLL 必須執行取消 **註冊**。

## <a name="syntax"></a>語法


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

特定資料庫之通訊協定的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

網路監視器在將所有 capture 資訊傳遞給剖析器 DLL 之後，會呼叫取消 **註冊** 。 剖析器 DLL 必須針對剖析器所支援的每個通訊協定，執行取消 **註冊** 函式。

執行取消 **註冊** 時，剖析器 DLL 必須呼叫 [DestroyPropertyDatabase](destroypropertydatabase.md) 函式來釋放 [*屬性資料庫*](p.md) 資源。



| 如需相關資訊                                        | 請參閱                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                 |
| 剖析器 DLL 中包含的進入點。        | [剖析器 DLL 架構](parser-dll-architecture.md) |
| 如何執行取消 **註冊**  包含範例。     | [執行取消註冊](implementing-deregister.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




