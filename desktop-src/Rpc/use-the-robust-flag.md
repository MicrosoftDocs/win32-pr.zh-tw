---
title: 使用/robust 旗標
description: 一律使用/robust 參數編譯 .idl 檔。
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933378"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="05a77-103">使用/robust 旗標</span><span class="sxs-lookup"><span data-stu-id="05a77-103">Use the /robust Flag</span></span>

<span data-ttu-id="05a77-104">一律使用 [**/robust**](/windows/desktop/Midl/-robust) 參數編譯 .idl 檔。</span><span class="sxs-lookup"><span data-stu-id="05a77-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="05a77-105">使用 **/robust** 參數會產生額外的資訊，讓網路資料表示 (NDR) 引擎，以在動態陣列、等位和 COM 和 RPC 應用程式的輸出介面指標中的相互關聯引數上執行執行時間錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="05a77-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="05a77-106">如果軟體無法使用此旗標進行編譯，軟體就會暴露在攻擊中，而不會在任何其他區域中進行保護。</span><span class="sxs-lookup"><span data-stu-id="05a77-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 