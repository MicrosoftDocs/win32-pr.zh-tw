---
title: 傳輸語法和 NDR64
description: NDR 網路通訊協定也稱為傳輸語法，可讓 RPC 呼叫跨越網路。
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433e68689ec4c960adbb43ddc19ec3e9e37765db57cfe6bf87c86c096720b771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011226"
---
# <a name="transfer-syntax-and-ndr64"></a>傳輸語法和 NDR64

NDR 網路通訊協定也稱為傳輸語法，可讓 RPC 呼叫跨越網路。 有線通訊協定會定義 RPC 呼叫的網路標記法，例如，資料成員的封送處理順序、網路上的資料對齊、資料中包含的額外資訊，以及其他問題。 NDR64 通訊協定是以32為基礎的 NDR 傳輸語法延伸模組，專門建立來讓開發人員以64位系統為目標，以達到最佳效能。

NDR 電傳格式和 NDR64 電傳格式之間的差異，會解決64位環境中不同指標的大小，以及其他問題。 NDR64 的機制是由 RPC 處理。 開發人員只需要使用/[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL 命令列參數，即可獲得 NDR64 在64位平臺上的優點。 NDR64 僅適用于64位平臺。

 

 