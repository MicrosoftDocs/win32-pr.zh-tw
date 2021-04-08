---
title: 開啟和關閉資料流程
description: 開啟和關閉資料流程
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream 函式
- AVIStreamRelease 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021164"
---
# <a name="opening-and-closing-streams"></a>開啟和關閉資料流程

開啟資料流程與開啟檔案類似。 您可以使用 [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) 函數來開啟資料流程。 此函式會建立資料流程介面、將資料流程的控制碼放在介面中，並將指標傳回至介面。 **AVIFileGetStream** 也會維護已開啟資料流程的應用程式參考計數，而不是已關閉它的應用程式的參考計數。

如果您想要存取檔案中的單一資料流程，您可以使用 [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) 函數來開啟檔案和資料流程。 此函數結合了 [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) 和 **AVIFileGetStream** 函數的作業和函式引數。

若要在檔案中存取一個以上的資料流程，請使用 **AVIFileOpen** 一次，然後再呼叫 **AVIFileGetStream** 的多個。

您可以使用 [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) 函式來遞增資料流程的參考計數，以在使用通常會關閉資料流程的函式時，讓資料流程保持開啟。

您可以使用 [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) 函數來關閉資料流程。 此函式會遞減資料流程的參考計數，並在參考計數到達零時將其關閉。 您的應用程式應在每次使用 [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)、 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)、 **AVIStreamAddRef** 或 **AVIStreamOpenFromFile** 函數時包含呼叫 **AVIStreamRelease** ，以平衡參考計數。 當您釋放使用 **AVIStreamOpenFromFile** 開啟的資料流程時，AVIFile 會關閉包含該資料流程的檔案。 如果您的應用程式釋出具有開啟資料流程的檔案，則 AVIFile 會等到所有資料流程都釋出之後，才會關閉資料流程。

 

 




