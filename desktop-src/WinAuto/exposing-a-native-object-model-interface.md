---
title: 公開原生物件模型介面
description: 如果 UI 元素支援 Microsoft Active Accessibility 或消費者介面自動化以外的原生物件模型，它可以回應 \_ 包含 OBJID NATIVEOM 物件識別碼的 WM GETOBJECT 訊息，藉以公開自訂介面 \_ 。
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644918"
---
# <a name="exposing-a-native-object-model-interface"></a>公開原生物件模型介面

如果 UI 元素支援 Microsoft Active Accessibility 或消費者介面自動化以外的原生物件模型，它可以回應包含 [**OBJID \_ NATIVEOM**](object-identifiers.md)物件識別碼的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息，藉以公開自訂介面。 若要回應，UI 元素應傳回 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式的呼叫所抓取的值。

用戶端可以藉由呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函式，並將 [**OBJID \_ NATIVEOM**](object-identifiers.md) 指定為第二個參數，從支援原生物件模型的 UI 元素取出介面。

 

 




