---
description: 剖析器的 DllMain 匯出函式會識別剖析器是否存在，並釋放網路監視器用於剖析器的資源。 DllMain 必須在所有剖析器 Dll 中實作為。
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: 'DllMain 剖析器回呼函數 (進程 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 5df58ef86971fcf60e79fbae8e92313dbd0b0371e2311cc30b494950e4f37dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890838"
---
# <a name="dllmain-parser-callback-function"></a>DllMain 剖析器回呼函數

剖析器的 **DllMain** 匯出函式會識別剖析器是否存在，並釋放網路監視器用於剖析器的資源。 **DllMain** 必須在所有剖析器 dll 中實作為。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hInstance* \[在\]
</dt> <dd>

剖析器實例的控制碼。

</dd> <dt>

*命令* \[在\]
</dt> <dd>

判斷如何呼叫函式的指標。 如需所有可能旗標的清單，請參閱 [DllMain](/windows/desktop/Dlls/dllmain)。 剖析器的執行必須處理下列值。



| 值                                                                                                                                                                         | 意義                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**DLL \_ 進程 \_ 附加**</dt> </dl> | 當您第一次呼叫 **DllMain** 時，DLL 必須呼叫 [CreateProtocol](createprotocol.md) 來提供網路監視器的資訊。 <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**DLL \_ 進程卸 \_ 離**</dt> </dl> | 當您最後一次呼叫 **DllMain** 時，dll 必須呼叫 [DESTROYPROTOCOL](destroyprotocol.md) 來釋放 DLL 使用的資源。 <br/> |



 

</dd> <dt>

*已保留* 
</dt> <dd>

目前未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

剖析器 DLL 一律會傳回 **TRUE**。

## <a name="remarks"></a>備註

作業系統會呼叫 **DllMain** 來載入和卸載剖析器 DLL。 這個函式是以動態連結程式庫 [DllMain](/windows/desktop/Dlls/dllmain) 函數為基礎。

您也可以使用 **DllMain** 的執行來儲存剖析器的實例，以供日後使用。 例如，您可以儲存剖析器 DLL 實例，然後將它用於未來的系統呼叫。



| 如需相關資訊                                        | 請參閱                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                  |
| 剖析器 DLL 中包含的進入點。        | [剖析器 DLL 架構](parser-dll-architecture.md)  |
| 如何執行 **DllMain**  包含範例。        | [執行 DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>處理。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

