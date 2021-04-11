---
description: CreateProtocol 函數會通知網路監視器有特定的通訊協定剖析器存在。
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: 'CreateProtocol 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115741"
---
# <a name="createprotocol-function"></a>CreateProtocol 函式

**CreateProtocol** 函數會通知網路監視器有特定的通訊協定剖析器存在。

## <a name="syntax"></a>語法


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolName* \[在\]
</dt> <dd>

剖析器將偵測到的通訊協定名稱。

</dd> <dt>

*lpEntryPoints* \[在\]
</dt> <dd>

[E](entrypoints.md)結構，其中包含其餘的剖析器 DLL 進入點。 如需每個進入點所參考的匯出函式清單，請參閱備註。 輸入點必須以 **e** 結構所指定的順序來提供。

</dd> <dt>

*cbEntryPoints* \[在\]
</dt> <dd>

**E** 結構的大小。 網路監視器提供 e \_ 大小宏，可讓您用來指定結構的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為通訊協定的控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

剖析器 DLL 會在其 [DllMain](dllmain-parser.md)的執行期間呼叫 **CreateProtocol** 。 當作業系統第一次載入剖析器 DLL 時，會呼叫 **CreateProtocol** 函數。

*LpEntryPoints* 參數中所參考的進入點包含下列匯出函式的指標，這些函式必須依照此處提供的順序提供。

-   [註冊](register-parser.md)
-   [取消註冊](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| 如需相關資訊                                                                                 | 請參閱                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。                                          | [解析 器](parsers.md)                                  |
| 如何執行 **dllmain** 包含在 **Dllmain** 內呼叫 **CreateProtocol** 的範例。 | [執行 DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

