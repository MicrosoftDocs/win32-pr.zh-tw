---
title: Run-Time 連結至 Wtsapi32.dll
description: 您的應用程式可以使用遠端桌面服務 API，在執行時間動態連結到 Wtsapi32.dll。 若要這樣做，您的應用程式應該呼叫 LoadLibrary 函式來載入 Wtsapi32.dll。
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc686f26029ee9bfa4332215e27a587a7e57b78de9bd0d1043ee58541ef76194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127493"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time 連結至 Wtsapi32.dll

如果您的應用程式是在不是遠端桌面服務環境的環境中執行，但您想要讓應用程式在遠端桌面服務環境中執行時提供額外的功能，應用程式可以使用遠端桌面服務 API 來執行額外的功能，並在執行時間以動態方式連結到 Wtsapi32.dll。 若要這樣做，您的應用程式應該呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Wtsapi32.dll。 如果 **LoadLibrary** 呼叫失敗，您的應用程式可以使用其基本功能來執行。 如果 **LoadLibrary** 成功，則您的應用程式可以呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以取得您想要呼叫之遠端桌面服務函式的指標。

如果您的應用程式僅適用于遠端桌面服務環境，則不需要動態連結。 在這種情況下，您可以包含 Wtsapi32.dll，並連結 Wtsapi32.dll .lib。 然後，如果您的應用程式在遠端桌面服務以外的環境中啟動，它將會結束，因為 Wtsapi32.dll 並不存在。

如需判斷您的應用程式是否正在遠端桌面服務環境中執行的相關資訊，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般程式設計指導方針](general-programming-guidelines.md)
</dt> </dl>

 

 