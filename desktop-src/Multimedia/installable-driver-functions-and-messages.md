---
title: 可安裝的驅動程式功能和訊息
description: 可安裝的驅動程式功能和訊息
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- 可安裝的驅動程式，函式
- 可安裝的驅動程式，訊息
- 可安裝的驅動程式，OpenDriver 函式
- OpenDriver 函式
- 可安裝的驅動程式、自訂訊息
- 驅動程式訊息
- 自訂驅動程式訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933199"
---
# <a name="installable-driver-functions-and-messages"></a>可安裝的驅動程式功能和訊息

您可以使用 [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) 函數，從應用程式開啟可安裝的驅動程式。 此函式會建立驅動程式的實例，如果沒有其他實例存在，則將驅動程式載入記憶體，並傳回新實例的控制碼。 開啟可安裝的驅動程式時，您必須提供驅動程式的完整路徑，或登錄機碼的名稱和與驅動程式相關聯的值。

開啟驅動程式之後，您可以使用 [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) 函式將驅動程式訊息傳送至驅動程式，指示它執行工作。 例如，您可以藉由傳送 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息，指示驅動程式顯示其設定對話方塊。 傳送此訊息之前，您必須藉由傳送 [**Winspool.drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) 訊息並檢查非零的傳回值，判斷驅動程式是否有設定對話方塊。 許多驅動程式都會提供一組自訂訊息，您可以傳送這些訊息來指示驅動程式的作業。

如果您需要可安裝驅動程式的特殊存取權（例如存取其資源），您可以使用 [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) 函式來取出驅動程式的模組控制碼。

當您不再需要可安裝的驅動程式時，您可以使用 [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) 函式將其關閉。

您可以使用可安裝的驅動程式功能和訊息來開啟和管理任何可安裝的驅動程式。 不過，開啟和管理多媒體裝置的建議動作是先使用標準服務 (例如，波形輸出裝置) 的 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)、 [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)和 [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) （如果有的話）。 如果多媒體驅動程式沒有標準服務存在，請使用可安裝的驅動程式功能和訊息來開啟和管理驅動程式。

> [!Note]  
> [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)和 [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)函數是用來將訊息傳送至驅動程式，以及取得模組實例控制碼的慣用函數。 不過，已包含舊版的 [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) 函式，以維持與舊版 Windows 作業系統的相容性。

 

 

 