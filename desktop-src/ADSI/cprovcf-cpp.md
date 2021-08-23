---
title: CPROVCF.CPP
description: 在範例提供者元件中，ADs 提供者物件 class factory 程式碼的一個程式碼範例位於 cprovcf .cpp 中。
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023666"
---
# <a name="cprovcfcpp"></a>CPROVCF.CPP

在範例提供者元件中，ADs 提供者物件 class factory 程式碼的一個程式碼範例位於 cprovcf .cpp 中。 提供者元件永遠不會直接建立此物件的實例，而不是在 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)中的系結作業期間，或在 **Visual Basic 方法的** 內建函式中自動建立物件。 下表列出支援的方法。



| 方法                                  | 描述                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF：： CreateInstance** | 為 ADS 提供者物件建立 class factory 的實例。 |



 

 

 




