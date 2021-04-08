---
description: 這個 TSPI \_ lineSetCurrentLocation 函式已淘汰。 當使用者 (使用 [撥號內容] 對話方塊) 或使用 lineSetCurrentLocation 函式 (的應用程式) 變更位址轉譯位置時，會呼叫此功能。
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693311"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

這個 TSPI \_ lineSetCurrentLocation 函式已淘汰。 當使用者 (使用 [ **撥號** 內容] 對話方塊) 或使用 [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) 函式 (的應用程式) 變更位址轉譯位置時，會呼叫此功能。

目前，轉譯位置的變更會產生一行 \_ DEVSTATE 訊息，並將 *dwParam1* 設定為 LINEDEVSTATE \_ TRANSLATECHANGE。

 

 
