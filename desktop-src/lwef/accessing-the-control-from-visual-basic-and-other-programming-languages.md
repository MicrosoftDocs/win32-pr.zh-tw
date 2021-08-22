---
title: 從 Visual Basic 和其他程式設計語言存取控制項
description: 從 Visual Basic 和其他程式設計語言存取控制項
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976858"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>從 Visual Basic 和其他程式設計語言存取控制項

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

您也可以從 Visual Basic 和其他程式設計語言使用 Microsoft Agent 的控制權。 請確定語言完全支援 ActiveX control 介面，並遵循其新增和存取 ActiveX 控制項的慣例。 若要存取此控制項，您必須已在目標系統上安裝代理程式。

然後，您可以從網站下載代理程式的自我安裝封包檔 (使用 [儲存而非執行] 選項) 。 您可以在安裝安裝程式中包含此檔案。 每次執行時，它就會在目標系統上自動安裝代理程式。 如需安裝的詳細資訊，請參閱 Microsoft 代理程式散發授權合約。 不支援使用代理程式自行安裝封包檔（例如嘗試複製和註冊代理程式元件檔）進行安裝。 這可確保一致且完全的安裝。 請注意，microsoft 代理程式自行安裝檔案不會安裝在 microsoft Windows 2000 上，因為該版本的作業系統已包含自己的代理程式版本。

若要成功在目標系統上安裝代理程式，您也必須確定目標系統有最新版本的 Microsoft Visual C++ 執行時間 (Msvcrt.dll) 、microsoft 註冊工具 (Regsvr32.dll) 和 Microsoft COM dll。 若要確保目標系統上的必要元件，最簡單的方式就是要求安裝 Microsoft Internet Explorer 3.02 或更新版本。 或者，您可以安裝 Microsoft Visual C++ 中提供的前兩個元件。 必要的 COM dll 可以安裝為 Microsoft DCOM update 的一部分，可在 Microsoft 網站上取得。 您可以在 Microsoft 網站上找到這些元件的進一步資訊和授權資訊。

代理程式的語言元件可以用同樣的方式來安裝。 同樣地，您可以使用這項技術，來安裝可從 Microsoft 代理程式網站散發的 Microsoft 字元 ACS 格式。 字元檔會自動安裝到 Microsoft 代理程式 \\ 字元子目錄。

因為 Microsoft 代理程式的元件是設計為作業系統元件，所以代理程式可能不會卸載。 同樣地，當代理程式已安裝為 Windows 作業系統的一部分時，代理程式自行安裝封包可能無法安裝。

 

 




