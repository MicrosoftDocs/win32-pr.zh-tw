---
description: Stream 控制項
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Stream 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850359"
---
# <a name="stream-control"></a>Stream 控制項

VMR 的輸入 pin () s 的 [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) 介面，可讓應用程式和上游篩選器控制混音器元件的行為，包括 Z 順序和 VMR 輸入資料流程的作用中狀態。 雖然此介面是在針腳上公開，但它會在 VMR 的混音器元件上運作，因此只有在載入混音器時才可使用，這是當 VMR 處理多個輸入資料流程時。 上游篩選器會使用 [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) 和 [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) 方法來控制來源色彩索引鍵。 這些方法會啟用像是動畫在影片上重迭的效果。 只要將色彩索引鍵設定為動畫資料流程的背景色彩，VMR 就會將該資料流程與另一個影片資料流程混合。 應用程式應該小心不要將色彩索引鍵變更為與上游篩選器所使用的值不同的值，例如解碼器。

篩選器會使用 [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) 和 [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) 方法，告知混音器是否預期輸入來自指定 pin 的輸入資料。 例如，Line21 解碼器只會在資料流程中有該資料時，使用這些方法來啟用 Line21 資料的 VMR 輸入 pin。 將 pin 設定為非作用中狀態，會指示混音器不要等待指定 pin 的資料，然後再組合影像。

 

 



