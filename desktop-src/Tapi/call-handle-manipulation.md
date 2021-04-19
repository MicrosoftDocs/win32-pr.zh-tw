---
description: TAPI 提供許多函數來操作呼叫控制碼、判斷行之間的關聯性、呼叫和位址等等。
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: 呼叫控制碼操作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991844"
---
# <a name="call-handle-manipulation"></a>呼叫控制碼操作

TAPI 提供許多函數來操作呼叫控制碼、判斷行之間的關聯性、呼叫和位址等等。 除了 [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)之外，大部分的功能都是在不參考服務提供者的情況下，嚴格地在 TAPI 內執行。 此函式會在其行內取出現有呼叫的位址識別碼。 以一組位址識別碼分組的服務提供者可以針對新的輸入或輸出呼叫選擇無法預期的位址。 當使用 LINECALLSELECT ADDRESS 選項叫用 [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) 作業時，此函式會提供 TAPI 足夠的資訊來執行該作業 \_ 。

 

 
