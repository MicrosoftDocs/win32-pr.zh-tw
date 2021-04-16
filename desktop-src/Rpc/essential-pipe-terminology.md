---
title: 基本管道術語
description: 如同遠端程序呼叫的其他參數類型，管道可以是 \ 或 \t 參數。
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508068"
---
# <a name="essential-pipe-terminology"></a>基本管道術語

如同遠端程序呼叫的其他參數類型，管道可以是 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。 由於伺服器會控制透過管道傳送資料的方式，因此會將具有 \[ **in** \] 屬性的管道 *提取* 至伺服器。 同樣地，輸出管道會從伺服器將資料 *推送* 至用戶端。 進行資料傳輸的程式分別稱為 *提取* 程式和 *推送* 程式。

MIDL 編譯器會產生伺服器的推播和提取程式。 此外，它也會管理記憶體中資料緩衝區的配置。 不過，用戶端必須提供自己的推播和提取程式。 它也必須提供程式來配置管道所使用的記憶體緩衝區。 用戶端 stub 會在適當的時間自動呼叫這些。 配置程式通常稱為配置程式或配置函數。

 

 