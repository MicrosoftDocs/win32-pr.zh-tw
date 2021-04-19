---
description: Register 匯出函式必須在所有剖析器 Dll 中實作為。 註冊的執行會建立並填入通訊協定的屬性資料庫。 網路監視器會使用資料庫來判斷通訊協定支援的屬性。
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: '將剖析器回呼函式註冊 (Netmon. h) '
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
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974624"
---
# <a name="register-parser-callback-function"></a>註冊剖析器回呼函數

**Register** 匯出函式必須在所有剖析器 dll 中實作為。 **註冊** 的執行會建立並填入通訊協定的 [*屬性資料庫*](p.md)。 網路監視器會使用資料庫來判斷通訊協定支援的屬性。

## <a name="syntax"></a>語法


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

呼叫 **Register** 時網路監視器提供的通訊協定控制碼。 呼叫匯出 helper 函式時，需要 *hProtocol* 控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

一旦載入 capture，網路監視器開始呼叫 **Register** 函數。 網路監視器會針對它可以識別的每個通訊協定呼叫 **Register** 函數。 [CreateProtocol](createprotocol.md)函式會將指標傳遞至 **Register** 函數。

**註冊** 的執行包含對下列函數的呼叫。

-   呼叫 [CreatePropertyDatabase](createpropertydatabase.md) 和 [AddProperty](/previous-versions/bb251873(v=msdn.10)) 函式，以建立該通訊協定支援之所有屬性的資料庫。
-   如果通訊協定使用 [*遞交集*](h.md)，則需要呼叫 [CreateHandoffTable](createhandofftable.md)函數。

如果剖析器 DLL 包含多個剖析器，且剖析器可以偵測到一個以上的通訊協定，您必須針對每個通訊協定執行 **Register** 函式。



| 的相關資訊                                        | 請參閱                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                 |
| 剖析器 DLL 中包含的進入點。        | [剖析器 DLL 架構](parser-dll-architecture.md) |
| 如何執行 **註冊**  包含範例。       | [執行註冊](implementing-register.md)     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

