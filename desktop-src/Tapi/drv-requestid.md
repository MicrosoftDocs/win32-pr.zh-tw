---
description: WINSPOOL.DRV \_ REQUESTID 資料類型是用來提供服務提供者要求的唯一識別碼。
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987528"
---
# <a name="drv_requestid"></a>WINSPOOL.DRV \_ REQUESTID

**Winspool.drv \_ REQUESTID** 資料類型是用來提供服務提供者要求的唯一識別碼。 此類型的值會以參數的形式傳遞至允許非同步作業的每個函數。 如果作業是非同步，服務提供者會傳回此值做為函數的傳回值。 每當服務提供者以非同步方式將要求標示為非同步時，它最後必須藉由呼叫 [*完成 \_*](/windows/win32/api/tspi/nc-tspi-async_completion) 程式回呼函式來回報作業已完成。

TAPI 可確保它所提供的 **Winspool.drv \_ REQUESTID** 值絕對是正面的，也就是在0x00000001 和0x7fffffff 之間的值（含）之間。 此外，這些值是唯一的，因為在作業回報完成之前，將會重複使用函式從函式傳回的值，以將要求標示為非同步。

 

 
