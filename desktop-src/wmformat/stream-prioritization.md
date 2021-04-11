---
title: 資料流程優先順序
description: 資料流程優先順序
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK，資料流程優先順序
- Advanced Systems Format (ASF) 、串流優先順序
- ASF (Advanced 系統格式) 、串流優先順序
- Windows Media 格式 SDK，資料流程的優先權順序
- Advanced Systems Format (ASF) ，資料流程的優先順序順序
- ASF (Advanced Systems Format) ，資料流程的優先順序順序
- 資料流程，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023058"
---
# <a name="stream-prioritization"></a>資料流程優先順序

當您建立 ASF 檔案時，可以為其組成的資料流程指定優先權順序。 如果您串流處理優先順序的檔案，而且可用的頻寬不足以傳遞所有資料流程，則讀取器會以反向優先權順序來卸載資料流程。 如此一來，您可以確保檔案中最重要的資料流程不會因為網路問題而卸載。

資料流程優先順序設定是以資料流程優先順序物件來設定，並新增至設定檔。 設定檔只能包含一個資料流程優先順序物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**IWMStreamPrioritization 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**使用資料流程優先順序**](using-stream-prioritization.md)
</dt> </dl>

 

 




