---
description: 目前，呼叫的所有時間都是由應用程式所剩餘。
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: 撥號狀態計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972452"
---
# <a name="call-state-timer"></a>撥號狀態計時器

目前，呼叫的所有時間都是由應用程式所剩餘。 如果應用程式監視大量的呼叫，而如果有多個應用程式存在（可能在多部伺服器上），則可能需要在相同的呼叫上維護計時器，才能讓這項工作變得很繁瑣。 因此，伺服器會處理撥號狀態的時間更有意義。

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **tStateEntryTime** 成員允許回報狀態中的呼叫時間。 **SYSTIME** 類型的成員 () 表示輸入目前狀態的時間。

 

 



