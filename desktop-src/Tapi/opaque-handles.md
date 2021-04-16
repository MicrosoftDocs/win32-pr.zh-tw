---
description: TSPI 所定義的一些類型是不透明的控制碼。
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: 不透明控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512060"
---
# <a name="opaque-handles"></a>不透明控制碼

TSPI 所定義的一些類型是不透明的控制碼。 這些會在 TSPI 中用來做為私用資料結構的公用參考。 這可讓您針對介面程式提供的參數進行類型檢查，同時仍然提供類型保護的量值。 只有私用資料結構的擁有者知道如何將不透明的型別解讀為其資料結構標記法的參考。 如需如何使用不透明控制碼的範例，請考慮使用電話裝置。 TAPI 和服務提供者通常會維護代表其個別裝置觀點的資料結構。

在 TAPI 和服務提供者所維護的一般電話資料結構中，每個都包含其他資料結構的不透明控制碼。 這些都是在早期的初始化步驟中進行交換。 當 TAPI 呼叫 TSPI 函式時，它會傳遞不透明的控制碼來參考裝置。 服務提供者知道如何將此解析為參考 (箭號) 至其資料結構。 當服務提供者在 TAPI 中呼叫回呼函式時，就會發生類似的進程。

 

 



