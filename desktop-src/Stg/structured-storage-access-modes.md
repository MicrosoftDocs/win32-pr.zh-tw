---
title: 結構化儲存體存取模式
description: 控制多個進程和使用者同時存取物件的機制是不可或缺的。
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、API 函式、用於存取的旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968624"
---
# <a name="structured-storage-access-modes"></a>結構化儲存體存取模式

控制多個進程和使用者同時存取物件的機制是不可或缺的。 COM 藉由定義儲存體和資料流程物件的存取模式，提供這些機制。 針對父儲存物件所指定的存取模式是由其子系所繼承，不過您可以對子系儲存體或串流進行額外的限制。 嵌套的儲存或資料流程物件可以在相同的模式下開啟，或以比其父系更受限制的模式開啟，但無法在不受限制的模式下開啟。

您可以使用 [**STGM 常數**](stgm-constants.md)中所列的值來指定存取模式。 這些值可作為要當做引數傳遞給 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面和相關 API 函式中之方法的旗標。 通常會使用布林值 **或** 運算，在參數 *grfMode* 中結合數個旗標。

旗標分為六個群組。 一次只能指定每個群組中的一個旗標：

-   [交易旗標](transaction-flags.md)
-   [儲存體建立旗標](storage-creation-flags.md)
-   [暫時建立旗標](temporary-creation-flags.md)
-   [優先權旗標](priority-flags.md)
-   [存取權限旗標](access-permission-flags.md)
-   [共用存取旗標](shared-access-flags.md)

 

 




