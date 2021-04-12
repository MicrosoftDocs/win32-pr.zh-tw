---
description: ParserAutoInstallInfo export 函數會識別位於 DLL 中的剖析器或剖析器。 ParserAutoInstallInfo 應該在所有剖析器 Dll 中實作為。
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: 'ParserAutoInstallInfo 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318072"
---
# <a name="parserautoinstallinfo-callback-function"></a>ParserAutoInstallInfo 回呼函式

**ParserAutoInstallInfo** export 函數會識別位於 DLL 中的剖析器或剖析器。 **ParserAutoInstallInfo** 應該在所有剖析器 dll 中實作為。

## <a name="syntax"></a>語法


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>參數

這個回呼函數沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是用來描述 DLL 中剖析器的 [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) 結構。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

當網路監視器第一次載入時，它會呼叫 **ParserAutoInstallInfo** (（如果存在的話）) 自動安裝每個剖析器，然後列舉剖析器子目錄中的所有剖析器 dll。

在 **PF \_ PARSERDLLINFO** 結構中傳回的資訊包括下列各項：

-   DLL 中的剖析器數目 (通常是一個) 。
-   每個剖析器偵測到的通訊協定名稱和簡短描述。
-   每個通訊協定都有選擇性的說明檔。
-   每個通訊協定前面的通訊協定。
-   遵循每個通訊協定的通訊協定。

每個剖析器 DLL 都應該包含一個剖析器。 不過，網路監視器可讓您建立包含一個以上剖析器的 DLL。 例如，tcpip.dll 是具有一個以上剖析器的網路監視器 DLL。



| 如需相關資訊                                               | 請參閱                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。        | [解析 器](parsers.md)                                                       |
| 剖析器 DLL 中包含的進入點。               | [剖析器 DLL 架構](parser-dll-architecture.md)                       |
| 如何執行 **ParserAutoInstallInfo**  包含範例。 | [執行 ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




