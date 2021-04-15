---
title: CPROVCF.Cpp
description: 在範例提供者元件中，ADs 提供者物件 class factory 程式碼的一個程式碼範例位於 cprovcf .cpp 中。
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461993"
---
# <a name="cprovcfcpp"></a>CPROVCF.Cpp

在範例提供者元件中，ADs 提供者物件 class factory 程式碼的一個程式碼範例位於 cprovcf .cpp 中。 提供者元件永遠不會直接建立此物件的實例，而不是在 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 中的系結作業期間，或在 **Visual Basic 方法的** 內建函式中自動建立物件。 下表列出支援的方法。



| 方法                                  | 描述                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF：： CreateInstance** | 為 ADS 提供者物件建立 class factory 的實例。 |



 

 

 




