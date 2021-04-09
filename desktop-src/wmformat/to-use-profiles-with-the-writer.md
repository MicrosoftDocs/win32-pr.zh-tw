---
title: 將設定檔與寫入器搭配使用
description: 將設定檔與寫入器搭配使用
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK，寫入 ASF 檔案
- Windows Media Format SDK，建立 ASF 檔案
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，寫入檔案
- ASF (Advanced Systems Format) ，寫入檔案
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
- 設定檔，建立 ASF 檔案
- 設定檔，寫入 ASF 檔案
- 設定檔，ASF 檔案建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023161"
---
# <a name="to-use-profiles-with-the-writer"></a>將設定檔與寫入器搭配使用

寫入器會使用設定檔資料來建立 ASF 檔案。 您必須指定要使用的設定檔，才能使用寫入器進行任何其他動作。

您可以藉由將設定檔識別碼傳遞給 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) 方法，來設定要搭配寫入器使用的系統設定檔。

若要指定要與寫入器搭配使用的自訂設定檔，您必須為包含所需設定檔資料的物件取得 [**IWMProfile**](iwmprofile.md) 介面。 您可以使用其中一個 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面的載入方法來完成這項工作。 當您有有效的 **IWMProfile** 介面之後，您可以將其指標傳遞至 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 方法。 如需設定檔設定的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。

如果您在設定寫入器中的設定檔之後，使用 **IWMProfile** 介面變更設定檔物件，您必須再次呼叫 **SetProfile** ，否則這些變更不會反映在寫入器中。 不過，呼叫 **SetProfile** 會重設所有的標頭屬性，因此請務必在呼叫這個方法之後設定任何必要的標頭屬性。

下列範例函式會將設定檔設定為「Windows Media 視訊8（適用于撥號數據機 (56 Kbps) 」）：


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> 沒有使用 Windows Media 音訊和 Video 9 系列編解碼器的預先定義系統設定檔。 如需詳細資訊，請參閱 [重複使用串流](reusing-stream-configurations.md)設定。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




