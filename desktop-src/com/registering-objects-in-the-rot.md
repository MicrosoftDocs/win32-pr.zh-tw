---
title: 在 ROT 中註冊物件
description: 在 ROT 中註冊物件
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372239"
---
# <a name="registering-objects-in-the-rot"></a>在 ROT 中註冊物件

一般來說，當用戶端要求伺服器建立物件實例時，伺服器通常會建立物件的標記，並透過 [**IRunningObjectTable：： Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register)的呼叫，將它註冊在執行中的物件資料表 (的 ROT) 。

當伺服器呼叫 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) 來建立要在 ROT 中註冊的檔案標記時，伺服器應該傳遞以磁片磁碟機為基礎，而非 UNC 格式的本機檔案名。 這可確保在遠端用戶端上執行衰減查閱時，由 ROT 暫存器呼叫所產生的標記比較資料將符合所使用的結果。 這是因為當分散式 COM 服務從遠端用戶端接收到伺服器本機檔案的啟用要求時，該檔案會轉換成以本機磁片磁碟機為基礎的路徑。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安裝為服務應用程式](installing-as-a-service-application.md)
</dt> <dt>

[在安裝時註冊類別](registering-a-class-at-installation.md)
</dt> <dt>

[註冊正在執行的 EXE 伺服器](registering-a-running-exe-server.md)
</dt> <dt>

[自我註冊](self-registration.md)
</dt> </dl>

 

 




