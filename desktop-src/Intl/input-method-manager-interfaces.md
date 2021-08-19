---
description: 本節說明 IMM 介面。
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: 輸入方法管理員介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e7267f5f38bb160a7f71b4f0379a2b03a3263b85a64dc8e666226dd3150911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809997"
---
# <a name="input-method-manager-interfaces"></a>輸入方法管理員介面

本節說明 IMM 介面。



| 介面                                                            | 描述                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | 提供不同語言通用的 IME 相關服務。                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | 允許用戶端存取 Microsoft IME 使用者字典。                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | 使用 Microsoft IME 提供語言處理服務。                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | 從 IMEPadApplets 執行 [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) 介面的應用程式中插入文字。                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | 透過 [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) 介面將字串輸入應用程式。                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | 提供對 IME 外掛程式字典清單的存取權。                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | 指定從 [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) 介面物件呼叫的方法，以模擬 [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) 介面。 |



 

 

 



