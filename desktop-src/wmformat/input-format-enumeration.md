---
title: 輸入格式列舉
description: 輸入格式列舉
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows媒體格式 SDK，輸入格式列舉
- Windows媒體格式 SDK，列舉輸入格式
- Advanced Systems Format (ASF) 、輸入格式列舉
- ASF (Advanced 系統格式) 、輸入格式列舉
- Advanced Systems Format (ASF) ，列舉輸入格式
- ASF (Advanced 系統格式) ，列舉輸入格式
- 輸入格式列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809038"
---
# <a name="input-format-enumeration"></a>輸入格式列舉

寫入器物件會從您提供的設定檔取得串流格式資訊。 設定檔中的串流設定資訊可為寫入器提供在檔案中寫入資料所需的所有資訊。 設定檔不會提供有關您的應用程式所提供之輸入範例格式的任何資訊給寫入器。 只有使用其中一個 Windows 媒體編解碼器壓縮的資料流程才會知道輸入格式：您可以根據設定檔中的資訊來預測任意資料流程類型的輸入。

寫入器物件可以與資料流程的編解碼器進行通訊，以判斷可以使用的輸入類型。 提供方法來列舉可能的輸入類型。 您應該一律尋找符合輸入媒體的輸入類型，方法是列舉支援的類型，而不是手動設定輸入媒體屬性。 如需詳細資訊，請參閱 [來列舉輸入格式](to-enumerate-input-formats.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案寫入功能**](file-writing-features.md)
</dt> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> </dl>

 

 




