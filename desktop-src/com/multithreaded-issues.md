---
title: 多執行緒問題
description: 多執行緒問題
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918528"
---
# <a name="multi-threaded-issues"></a>多執行緒問題

OLE 提供多執行緒應用程式的支援，可讓應用程式從多個執行緒進行 OLE 呼叫。 此多執行緒支援稱為「單元模型」，因此使用多個執行緒的所有 OLE 元件都必須遵循此模型。 單元模型要求 (使用 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)將介面指標封送處理，並線上程之間傳遞時 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> </dl>

 

 




