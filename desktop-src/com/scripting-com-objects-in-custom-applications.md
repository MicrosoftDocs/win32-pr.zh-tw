---
title: 在自訂應用程式中編寫 COM 物件的腳本
description: 在自訂應用程式中編寫 COM 物件的腳本
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9fb24c9e1df0cded5d648be70f8ae2582a54517b8b7eda35d1b972e44ca6c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372888"
---
# <a name="scripting-com-objects-in-custom-applications"></a>在自訂應用程式中編寫 COM 物件的腳本

Microsoft 提供數個用於撰寫 COM 物件腳本的環境： Active Server Pages、Windows Script Host 等等。 獨立軟體廠商 (Isv) 也可以授權 Microsoft 腳本引擎在其應用程式中使用。 例如，建立字組處理器的 ISV 可能會想要在應用程式中加入宏語言，讓使用者可以將簡單的工作自動化。 藉由授權腳本引擎，ISV 可以使用 VBScript 或 JScript 之類的語言作為應用程式的宏語言。

除了授權 VBScript 和 JScript 腳本引擎之外，isv 還可以撰寫自己的 ActiveX 腳本引擎。 然後，這些腳本引擎可以插入任何支援 ActiveX 腳本引擎標準的主機環境中。 例如，ISV 可能會撰寫 PerlScript 腳本引擎，並將它安裝在 ASP 伺服器上，因此可讓 ASP 伺服器處理 PerlScript 腳本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 COM 物件編寫腳本](scripting-with-com-objects.md)
</dt> </dl>

 

 




