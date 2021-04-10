---
title: 在自訂應用程式中編寫 COM 物件的腳本
description: 在自訂應用程式中編寫 COM 物件的腳本
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183394"
---
# <a name="scripting-com-objects-in-custom-applications"></a>在自訂應用程式中編寫 COM 物件的腳本

Microsoft 提供數個用於編寫 COM 物件腳本的環境： Active Server Pages、Windows Script Host 等等。 獨立軟體廠商 (Isv) 也可以授權 Microsoft 腳本引擎在其應用程式中使用。 例如，建立字組處理器的 ISV 可能會想要在應用程式中加入宏語言，讓使用者可以將簡單的工作自動化。 藉由授權腳本引擎，ISV 可以使用 VBScript 或 JScript 之類的語言作為應用程式的宏語言。

除了授權 VBScript 和 JScript 腳本引擎之外，Isv 還可以撰寫自己的 ActiveX 腳本引擎。 然後，這些腳本引擎可以插入任何支援 ActiveX 腳本引擎標準的主機環境中。 例如，ISV 可能會撰寫 PerlScript 腳本引擎，並將它安裝在 ASP 伺服器上，因此可讓 ASP 伺服器處理 PerlScript 腳本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 COM 物件編寫腳本](scripting-with-com-objects.md)
</dt> </dl>

 

 




