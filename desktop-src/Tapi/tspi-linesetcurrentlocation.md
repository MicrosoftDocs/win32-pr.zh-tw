---
description: 這個 TSPI \_ lineSetCurrentLocation 函式已淘汰。 當使用者 (使用 [撥號內容] 對話方塊) 或使用 lineSetCurrentLocation 函式 (的應用程式) 變更位址轉譯位置時，會呼叫此功能。
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012118"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

這個 TSPI \_ lineSetCurrentLocation 函式已淘汰。 當使用者 (使用 [ **撥號** 內容] 對話方塊) 或使用 [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) 函式 (的應用程式) 變更位址轉譯位置時，會呼叫此功能。

目前，轉譯位置的變更會產生一行 \_ DEVSTATE 訊息，並將 *dwParam1* 設定為 LINEDEVSTATE \_ TRANSLATECHANGE。

 

 
