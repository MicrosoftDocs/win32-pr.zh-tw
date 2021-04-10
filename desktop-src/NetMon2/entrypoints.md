---
description: E 結構定義了匯出函式的進入點，這些函數網路監視器用來操作剖析器。
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: 'E 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936640"
---
# <a name="entrypoints-structure"></a>E 結構

**E** 結構定義了匯出函式的進入點，這些函數網路監視器用來操作剖析器。

## <a name="syntax"></a>語法


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>成員

<dl> <dt>

**註冊**
</dt> <dd>

[*註冊專家*](register-expert.md)函式的實作為指標。

</dd> <dt>

**取消註冊**
</dt> <dd>

取消 [**註冊**](deregister.md) 函式之執行的指標。

</dd> <dt>

**RecognizeFrame**
</dt> <dd>

[**RecognizeFrame**](recognizeframe.md)匯出函式之執行的指標。

</dd> <dt>

**AttachProperties**
</dt> <dd>

[**AttachProperties**](attachproperties.md)匯出函式之執行的指標。

</dd> <dt>

**FormatProperties**
</dt> <dd>

[**FormatProperties**](formatproperties.md)匯出函式之執行的指標。

</dd> </dl>

## <a name="remarks"></a>備註

**CreateProtocol** 函式會使用 **e** 結構來提供網路監視器的指標。 指標必須依照 [先前成員] 區段中所識別的順序來指定。

如果網路監視器絕不會顯示通訊協定資料，則不需要執行 [**FormatProperties**](formatproperties.md) 函式。 例如，如果匯出應用程式使用剖析器的輸出，則不需要執行 **FormatProperties** ，而且網路監視器不會顯示輸出。



| 如需相關資訊                                        | 請參閱                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                  |
| 如何執行 **DllMain**  包含範例。        | [執行 DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[AttachProperties](attachproperties.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[取消註冊](deregister.md)
</dt> <dt>

[FormatProperties](formatproperties.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> <dt>

[註冊](register-parser.md)
</dt> </dl>

 

 




