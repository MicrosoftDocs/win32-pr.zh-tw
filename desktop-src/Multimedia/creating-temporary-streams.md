---
title: 建立暫存資料流程
description: 建立暫存資料流程
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate 函式
- AVIStreamRelease 函式
- AVIMakeCompressedStream 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462184"
---
# <a name="creating-temporary-streams"></a>建立暫存資料流程

暫存串流有很大的好處。 您可以使用暫存串流作為工作資料流程，例如，變更資料流程格式時。 或者，您可以建立暫存資料流程來保存部分已複製的資料流程。

您可以使用 [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) 函數，在記憶體中建立與任何檔案沒有關聯的資料流程。 此函式會將介面的位址傳回至指定位置中的新資料流程，並且由其他建立暫存資料流程的函式在內部使用。

您可以使用 [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) 函數，從未壓縮的資料流程建立壓縮的資料流程。 您可以識別要壓縮的資料流程、壓縮方法和壓縮選項，以及新資料流程的處理常式。

當您完成使用以 **AVIStreamCreate** 或 **AVIMakeCompressedStream** 建立的資料流程時，請使用 [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) 函數來關閉資料流程。 **AVIStreamRelease** 會釋出暫存資料流程所使用的資源。

 

 




