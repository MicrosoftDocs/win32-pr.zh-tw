---
title: 設定資料單位延伸模組
description: 設定資料單位延伸模組
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- 資料單位延伸模組，設定
- 資料流程，資料單位延伸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1bb88e9aa0c3bc00d4c21a1c262b7ff4a44fbc2f426f139b3b782a0bbdb7b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197480"
---
# <a name="setting-data-unit-extensions"></a>設定資料單位延伸模組

某些串流會設定為使用資料單位延伸模組，將補充資料與個別範例產生關聯。 如需擴充範例的詳細資訊，請參閱 [資料單位延伸](data-unit-extensions.md)。

大部分的資料單位延伸系統都需要在資料流程中的每個範例上有一個延伸模組。 如果您未提供正確大小的延伸，寫入器將會拒絕範例。

若要將擴充資料加入至範例，請使用 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法。 您可以使用 [**IWMStreamConfig2：： GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) 和 [**IWMStreamConfig2：： GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) 方法，取得有關資料流程上所設定之資料單位延伸模組的資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料單位延伸模組**](configuring-data-unit-extensions.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




