---
title: 取得編碼身分識別
description: 正在解碼編碼資料的應用程式，可以在呼叫常式將其解碼之前，取得用來將資料編碼的常式識別。 MesInqProcEncodingId 常式會提供此身分識別。
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- 遠端程序呼叫 RPC、工作、取得編碼身分識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a0883a1a032a76f13cfeeb6c5d6a8923146b7ee9e8184d37d5994fb5e328bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019445"
---
# <a name="obtaining-an-encoding-identity"></a>取得編碼身分識別

正在解碼編碼資料的應用程式，可以在呼叫常式將其解碼之前，取得用來將資料編碼的常式識別。 [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid)常式會提供此身分識別。

MIDL 編譯器會為介面中的每個程式指派一個整數識別碼，稱為程式 *識別碼* 或 *proc ID*。 編號開頭為零。 RPC 執行時間程式庫不涉及將程式識別碼轉譯為實際的程序呼叫。 指定 proc 識別碼之後，您的應用程式必須提供呼叫正確程式的方法。 一般來說，應用程式開發人員會在使用 C/c + + 時，使用一系列的 **if** 語句或 (，) 這個用途的 **switch** 語句。

 

 




