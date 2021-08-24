---
title: 壓縮和解壓縮的基本概念
description: 壓縮和解壓縮的基本概念
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，開啟壓縮機
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，開啟壓縮機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1969748949aeb023f889bc651ccd028f19c3e18fe6cf1ba088b4f4ec29292f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144991"
---
# <a name="compressor-and-decompressor-basics"></a>壓縮和解壓縮的基本概念

若要開啟並尋找壓縮的功能，您可以使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 和 [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) 函式。 您可以使用 **ICLocate** 來尋找特定類型的壓縮程式，並取得它的控制碼，以便在其他 bc-vcm-lvm-hyperv 函式中使用。 若要開啟壓縮壓縮，您可以使用 **ICOpen**。 當應用程式使用其他 BC-VCM-LVM-HYPERV 函式時，您的應用程式會使用這個函數所傳回的控制碼來識別開啟的壓縮程式。

若要開啟並尋找解壓縮程式，應用程式可以使用 [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) 和 [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) 宏。 這些宏會使用 **ICLocate** 來進行操作。

當您的應用程式已完成使用壓縮程式或解壓縮程式時，必須將其關閉，以釋放用於壓縮或解壓縮的任何資源。 您的應用程式可以使用 [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) 函數來關閉壓縮程式或解壓縮程式。

此外，您的應用程式也可以使用 [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) 函數來列舉系統上的壓縮機或 decompressors。

> [!Note]  
> AVI 檔案中的資料流程標頭包含資料流程類型的相關資訊，以及該資料流程的特定處理常式。 在資料流程標頭中， **fccType** 和 **fccHandler** 成員會識別資料流程類型以及為數據流指定的資料流程處理常式。

 

 

 




