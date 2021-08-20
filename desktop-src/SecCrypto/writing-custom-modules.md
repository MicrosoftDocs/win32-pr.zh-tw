---
description: 您可以用 C、c + + 或 Visual Basic 程式設計語言撰寫原則模組。
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: 撰寫自訂模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c9c07c074be48218d775acd75926ffbd4b7f04b1d6fc53a440dcc1e898c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970611"
---
# <a name="writing-custom-modules"></a>撰寫自訂模組

您可以用 C、c + + 或 Visual Basic 程式設計語言撰寫原則模組。 必要的 Microsoft 編譯器可在 Visual C++ 5.0 版或更新版本，或 Visual Basic 5.0 版或更新版本中使用。  (CA) 的企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位只能使用 Microsoft 提供的企業原則模組。

撰寫自訂原則模組時，您必須執行 [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) 。 此外，撰寫自訂原則模組時，您必須執行 [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) 。

原則模組可以從 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 呼叫方法，以協助處理 [*憑證要求*](../secgloss/c-gly.md); **ICertServerPolicy** 可讓您設定和抓取屬性和憑證延伸。

如需詳細資訊，請參閱下列主題。



| 主題                                                                      | 描述                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [設定憑證屬性](setting-certificate-properties.md)       | 設定憑證的屬性 |
| [撰寫自訂結束模組](writing-custom-exit-modules.md)             | 撰寫自訂結束模組             |
| [撰寫自訂延伸模組處理常式](writing-custom-extension-handlers.md) | 撰寫自訂延伸模組處理常式       |



 

 

 
