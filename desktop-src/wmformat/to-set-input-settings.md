---
title: 若要設定輸入設定
description: 若要設定輸入設定
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF) ，輸入設定
- ASF (Advanced Systems Format) ，輸入設定
- 設定檔，輸入設定
- 編解碼器，輸入設定
- 資料流程，輸入設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df5b10ea6bd15ad083b26a61af037527f00576eaa6b7e1fa795ea1591417ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447018"
---
# <a name="to-set-input-settings"></a>若要設定輸入設定

輸入媒體和串流媒體的基本屬性是由 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構所定義。 針對輸入格式，媒體類型資訊是由您的應用程式設定。 針對串流格式，媒體類型資訊會在您指派給寫入器的設定檔中設定。 有些屬性與媒體類型無關，而且必須在寫入開始之前為輸入設定。 這些屬性是獨立于資料流程類型的編解碼器和寫入器功能，而且必須在寫入器中指派設定檔之後，但在寫入開始之前設定。

設定輸入設定需要呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)。 您也可以使用 [**IWMWriterAdvanced2：： GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)的呼叫來檢查設定的目前值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將設定檔與寫入器搭配使用**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> <dt>

[**寫入影像資料流程**](writing-image-streams.md)
</dt> </dl>

 

 




