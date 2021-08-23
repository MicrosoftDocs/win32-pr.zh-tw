---
title: 光線承載結構
description: 在 TraceRay 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565628"
---
# <a name="ray-payload-structure"></a>光線承載結構 

在 [**TraceRay**](traceray-function.md) 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數，其中包括 [任何命中](any-hit-shader.md)、 [最接近的點擊](closest-hit-shader.md)和 [遺漏](miss-shader.md) 著色器。 存取光線承載的任何著色器都必須使用與原始 **TraceRay** 呼叫所提供的相同結構。  即使其中一個著色器根本不參考光線承載，仍必須指定相符的裝載做為原始 **TraceRay** 呼叫。

