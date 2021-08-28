---
title: TraceLogging 包裝函式宏
description: 列出 TraceLogging 提供者的包裝函式宏。
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bad266f44dbd82c31ceea95eed2978c5634beb8a75830d073465ef11c1be331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966477"
---
# <a name="tracelogging-wrapper-macros"></a>TraceLogging 包裝函式宏

列出 TraceLogging 提供者的包裝函式宏。

若要使用 TraceLogging 提供者來記錄事件，您必須使用 TraceLogging 寫入宏 [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 或 [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)。 這兩個宏都需要您將任何事件資料包裝在包裝函式宏中。 不同的資料類型有幾個不同的包裝函式宏。 如需 TraceLogging 宏的完整清單，請參閱 [TraceLogging 宏](trace-logging-macros.md)。

除了上述的包裝函式宏之外，還提供數個宏供個別資料類型使用。 所有這些宏都具有與 [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) 宏相同的格式。 您可以使用 TraceLoggingValue 宏來自動偵測要使用的適當包裝函式宏，或直接使用特定宏。

-   [**TraceLoggingBinary**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [**TraceLoggingChannel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [**TraceLoggingCustomAttribute**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [**TraceLoggingDescription**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [**TraceLoggingEventTag**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [**TraceLoggingKeyword**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [**TraceLoggingLevel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [**TraceLoggingOpcode**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [**TraceLoggingSocketAddress**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [**TraceLoggingStruct**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [**TraceLoggingValue**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> **TraceLoggingOptionGroup** 專用於 TRACELOGGING \_ 定義提供者內的使用 \_ 。
>
> -   [**TraceLoggingOptionGroup**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

以下是個別的包裝函式宏。

-   TraceLoggingInt8

-   TraceLoggingUInt8

-   TraceLoggingInt16

-   TraceLoggingUInt16

-   TraceLoggingInt32

-   TraceLoggingUInt32

-   TraceLoggingInt64

-   TraceLoggingUInt64

-   TraceLoggingFloat32

-   TraceLoggingFloat64

-   TraceLoggingBool

-   TraceLoggingFileTime

-   TraceLoggingGuid

-   TraceLoggingPointer

-   TraceLoggingSystemTime

-   TraceLoggingHexInt8

-   TraceLoggingHexUInt8

-   TraceLoggingHexInt32

-   TraceLoggingHexUInt32

-   TraceLoggingHexInt64

-   TraceLoggingHexUInt64

-   TraceLoggingWchar

-   TraceLoggingChar

-   TraceLoggingIntPtr

-   TraceLoggingUIntPtr

-   TraceLoggingBoolean

-   TraceLoggingHexInt16

-   TraceLoggingHexUInt16

-   TraceLoggingPid

-   TraceLoggingTid

-   TraceLoggingPort

-   TraceLoggingWinError

-   TraceLoggingNTStatus

-   TraceLoggingHResult

-   TraceLoggingSocketAddress

-   TraceLoggingSid

-   TraceLoggingString

-   TraceLoggingWideString

-   TraceLoggingCountedString

-   TraceLoggingCountedWideString

-   TraceLoggingAnsiString

-   TraceLoggingUnicodeString

-   TraceLoggingBinary (void \* 資料、資料大小（以位元組為單位）、 \[ 選擇性 \] 名稱 ) 這個宏的參數不同于上述的參數。 如果指定 *name* 參數，它必須是字串常值， (不是變數) ，而且可能不包含任何內嵌的 null 字元。 如果未提供 *名稱* 參數，則會自動產生名稱。

TraceLogging API 也會為數組提供數個宏。 這些陣列的長度可以是固定長度，也可以是可變長度的長度，視您選擇使用的包裝函式宏而定。 所有這些包裝函式宏都遵循此格式。

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

參數 *pVals* 指向資料的陣列，而 *cVals* 指出陣列中的元素數目。 *cVals* 必須是常數，而且不可以是變數。 如同單一值包裝函式宏， *name*、 **desc** 和 *tag* 是選擇性參數，且必須遵循與 **TraceLoggingValue** 宏所說明的相同限制。

-   TraceLoggingInt8FixedArray

-   TraceLoggingUInt8FixedArray

-   TraceLoggingInt16FixedArray

-   TraceLoggingUInt16FixedArray

-   TraceLoggingInt32FixedArray

-   TraceLoggingUInt32FixedArray

-   TraceLoggingInt64FixedArray

-   TraceLoggingUInt64FixedArray

-   TraceLoggingFloat32FixedArray

-   TraceLoggingFloat64FixedArray

-   TraceLoggingBoolFixedArray

-   TraceLoggingGuidFixedArray

-   TraceLoggingPointerFixedArray

-   TraceLoggingFileTimeFixedArray

-   TraceLoggingSystemTimeFixedArray

-   TraceLoggingHexInt8FixedArray

-   TraceLoggingHexUInt8FixedArray

-   TraceLoggingHexInt32FixedArray

-   TraceLoggingHexUInt32FixedArray

-   TraceLoggingHexInt64FixedArray

-   TraceLoggingHexUInt64FixedArray

-   TraceLoggingWcharFixedArray

-   TraceLoggingCharFixedArray

-   TraceLoggingIntPtrFixedArray

-   TraceLoggingUIntPtrFixedArray

-   TraceLoggingBooleanFixedArray

-   TraceLoggingHexInt16FixedArray

-   TraceLoggingHexUInt16FixedArray

-   TraceLoggingInt8Array

-   TraceLoggingUInt8Array

-   TraceLoggingInt16Array

-   TraceLoggingUInt16Array

-   TraceLoggingInt32Array

-   TraceLoggingUInt32Array

-   TraceLoggingInt64Array

-   TraceLoggingUInt64Array

-   TraceLoggingFloat32Array

-   TraceLoggingFloat64Array

-   TraceLoggingBoolArray

-   TraceLoggingGuidArray

-   TraceLoggingPointerArray

-   TraceLoggingFileTimeArray

-   TraceLoggingSystemTimeArray

-   TraceLoggingHexInt8Array

-   TraceLoggingHexUInt8Array

-   TraceLoggingHexInt32Array

-   TraceLoggingHexUInt32Array

-   TraceLoggingHexInt64Array

-   TraceLoggingHexUInt64Array

-   TraceLoggingWcharArray

-   TraceLoggingCharArray

-   TraceLoggingIntPtrArray

-   TraceLoggingUIntPtrArray

-   TraceLoggingBooleanArray

-   TraceLoggingHexInt16Array

-   TraceLoggingHexUInt16Array

 

 




