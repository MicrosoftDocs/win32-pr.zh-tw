---
title: 基底類型
description: 為了避免與執行相依的資料類型在不同的電腦架構上造成的問題，MIDL 定義了它自己的基底資料類型。
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316243"
---
# <a name="base-types"></a>基底類型

為了避免與執行相依的資料類型在不同的電腦架構上造成的問題，MIDL 定義了它自己的基底資料類型。



| 基底類型                         | Description                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | 可以有 **TRUE** 或 **FALSE** 值的資料項目。                                                                                                          |
| [**位元組**](/windows/desktop/Midl/byte)             | 在不進行任何變更的情況下，保證可以傳輸的8位資料項目。                                                                                                 |
| [**字元**](/windows/desktop/Midl/char-idl)         | 8位不帶正負號的字元資料項。                                                                                                                              |
| [**double**](/windows/desktop/Midl/double)         | 64位浮點數。                                                                                                                                     |
| [**浮動**](/windows/desktop/Midl/float)           | 32位浮點數。                                                                                                                                     |
| [**處理 \_ t**](/windows/desktop/Midl/handle-t)    | 可用於 RPC 系結或資料序列化的基本控制碼。                                                                                            |
| [**超**](/windows/desktop/Midl/hyper)           | 可以宣告為 [**帶正負**](/windows/desktop/Midl/signed)號或不 [**帶正負**](/windows/desktop/Midl/unsigned)號的64位整數也可以稱為 **\_ int64**。                  |
| [**int**](/windows/desktop/Midl/int)               | 可以宣告為 **帶正負** 號或不 **帶正負** 號的32位整數。                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | 關鍵字，指定具有32位或64位屬性的整數型別。                                                                              |
| [**long**](/windows/desktop/Midl/long)             | 整數的修飾 **詞，表示** 32 位整數。 可以宣告為 **帶正負** 號或不 **帶正負** 號。                                                       |
| [**short**](/windows/desktop/Midl/short)           | 可以宣告為 **帶正負** 號或不 **帶正負** 號的16位整數。                                                                                         |
| [**小**](/windows/desktop/Midl/small)           | 整數的修飾 **詞，表示** 8 位整數。 可以宣告為 **帶正負** 號或不 **帶正負** 號。                                                       |
| [**wchar \_ t**](/windows/desktop/Midl/wchar-t)      | 支援作為 IDL 之 Microsoft 延伸模組的寬字元類型。 因此，如果您使用 [ / **憑證**](/windows/desktop/Midl/-osf)參數進行編譯，則無法使用此類型。 |



 

標頭檔 Rpcndr 會提供大多數這些基底資料類型的定義。 關鍵字 **int** 可辨識，並在32位平臺上可。 在16位平臺上， **int** 資料類型需要修飾詞（例如 **簡短** 或 **long**）來指定它的長度。

雖然 **void \* \*** 會被 ANSI C 標準辨識為泛型指標類型，但 MIDL 會限制其使用方式。 遠端或序列化作業中使用的每個指標都必須指向基底類型或從基底類型所建立的類型。  (發生例外狀況：內容控制碼定義為 **void** 類型。 如需詳細資訊，請參閱 [內容控制碼](context-handles.md)。 ) 

 

 