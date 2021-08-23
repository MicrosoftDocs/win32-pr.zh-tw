---
title: 標頭檔
description: 標頭檔包含在 IDL 檔案中宣告之所有資料類型和作業的定義，以及在包含于-include 指示詞中的檔案中宣告的所有資料類型和作業。
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL 和 RPC MIDL、介面、標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582128"
---
# <a name="the-header-file"></a>標頭檔

標頭檔包含在 IDL 檔案中宣告之所有資料類型和作業的定義，以及包含在 include 指示詞中的檔案中宣告的所有資料類型和作業 \# 。 使用匯入指示詞彙入之檔案中的資料類型不會複寫至標頭檔;相反地，所產生的標頭檔會包含從匯入檔案產生之 H 檔案的包含行。 所有呼叫已定義作業的應用程式模組都必須包含標頭檔、執行定義的作業，或操作已定義的類型。

MIDL 編譯器參數 [**/header**](-header.md) 和 [**/out**](-out.md) 會影響標頭檔。

 

 




