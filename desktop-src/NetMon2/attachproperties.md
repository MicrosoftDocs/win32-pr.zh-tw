---
description: AttachProperties 匯出函式會將屬性對應到一段辨識的資料中的位置。 AttachProperties 必須針對剖析器 DLL 支援的每個剖析器來執行。
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: 'AttachProperties 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974261"
---
# <a name="attachproperties-callback-function"></a>AttachProperties 回呼函式

**AttachProperties** 匯出函式會將屬性對應到一段辨識的資料中的位置。 **AttachProperties** 必須針對剖析器 DLL 支援的每個剖析器來執行。

## <a name="syntax"></a>語法


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

正在剖析之框架的控制碼。

</dd> <dt>

*lpFrame* \[在\]
</dt> <dd>

框架中第一個位元組的指標。

</dd> <dt>

*lpProtocol* \[在\]
</dt> <dd>

已辨識資料開頭的指標。

</dd> <dt>

*MacType* \[在\]
</dt> <dd>

框架中第一個通訊協定的 MAC 值。 *MacType* 可以是下列其中一項：



| 值                                                                                                                                                                         | 意義                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**MAC \_ 類型 \_ ETHERNET**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**MAC \_ 類型 \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**MAC \_ 類型的 \_ FDDI**</dt> </dl>                | ANSI X3T 9。5 <br/> |



 

</dd> <dt>

*BytesLeft* \[在\]
</dt> <dd>

框架中剩餘的位元組數目，從已辨識的資料開頭開始。

</dd> <dt>

*hPreviousProtocol* \[在\]
</dt> <dd>

先前通訊協定的控制碼。

</dd> <dt>

*nPreviousProtocolOffset* \[在\]
</dt> <dd>

先前的通訊協定從框架開頭開始的位移。

</dd> <dt>

*lpInstData* \[在\]
</dt> <dd>

先前的通訊協定所提供之實例資料的指標。 實例資料的長度不能超過 DWORD \_ 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為框架中已辨識資料之後第一個位元組的指標，如果可辨識的資料是框架中的最後一個資料片段，則傳回 **Null** 。

如果函式不成功，則傳回值會是已辨識資料的指標。 *LpProtocol* 參數會將指標傳遞至剖析器 DLL。

## <a name="remarks"></a>備註

網路監視器會針對辨識框架中某部分資料的每個剖析器，呼叫 **AttachProperties** 函數。 請注意，剖析器會判斷哪些屬性存在於已辨識的資料中，以及每個屬性的所在位置。

在 **AttachProperties** 的執行期間，呼叫 [AttachPropertyInstance](attachpropertyinstance.md) 以使用存在於捕捉中的資料。 您也可以呼叫 [AttachPropertyInstanceEx](attachpropertyinstanceex.md) 函數來修改屬性資料。 不過，建議您使用存在於捕捉中的資料。

**AttachPropertyInstanceEx** 和 **AttachPropertyInstance** 函式只會針對存在於已辨識資料中的屬性進行呼叫。 請注意，網路監視器具有剖析器的 [*屬性資料庫*](p.md) ，其中包含剖析器所支援之所有屬性的描述。

**執行個體資料**

實例資料是從某個剖析器傳遞至另一個剖析器的資訊。 實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。 在 **AttachProperties** 和 [RecognizeFrame](recognizeframe.md)函式的 *lpInstData* 參數中，網路監視器提供上一個通訊協定的實例資料指標。 您可以在 **RecognizeFrame** 的執行期間，設定剖析器的實例資料。



| 如需相關資訊                                          | 請參閱                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。   | [解析 器](parsers.md)                                             |
| 剖析器 DLL 中包含了哪些進入點。           | [剖析器 DLL 架構](parser-dll-architecture.md)             |
| 如何辨識資料。                                      | [執行 RecognizeFrame](implementing-recognizeframe.md)     |
| 如何建立屬性資料庫。                          | [執行註冊](implementing-register.md)                 |
| 如何執行 **AttachProperties**  包含範例。 | [執行 AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




