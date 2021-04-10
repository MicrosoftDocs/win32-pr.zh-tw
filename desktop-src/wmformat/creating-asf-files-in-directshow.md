---
title: '在 DirectShow 中建立 ASF 檔案 (Windows Media Format 11 SDK) '
description: 在 DirectShow 中建立 ASF 檔案
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK，在 DirectShow 中建立 ASF 檔案
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，在 DirectShow 中建立
- ASF (Advanced Systems Format) ，在 DirectShow 中建立
- DirectShow，建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093615"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>在 DirectShow 中建立 ASF 檔案 (Windows Media Format 11 SDK) 

您可以使用 DirectShow 直接從捕捉來源（例如 DV 攝影機）建立 ASF 檔案，或將其他檔案轉碼成 Windows Media 格式。 在任一案例中，應用程式會建立包含 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器作為轉譯器的篩選圖形。

WM ASF 寫入器提供 Windows Media 格式 SDK 的部分包裝函式。 應用程式可以使用篩選器的 [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) 介面，將系統設定檔傳入 (4、7或 8) 的系統設定檔，或直接使用 Windows MEDIA 格式 SDK 來建立自訂設定檔，以傳遞至篩選準則。 若要加入中繼資料和其他標頭資訊，應用程式會使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面（可從篩選中取得）。 設定設定檔和中繼資料之後，應用程式就可以直接執行篩選圖形。 就內部而言，此篩選器會使用 Windows Media Format SDK 來寫入檔案。 此篩選器會處理所有音訊影片的同步處理詳細資料，而這也是應用程式的責任。

下列各節將更詳細地說明此程式。



| 區段                                                                                                           | 描述                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [設定 WM ASF 寫入器 (QASF) ](configuring-the-wm-asf-writer--qasf.md)                                   | 說明如何設定 WM ASF 寫入器篩選器。                                   |
| [建立篩選圖形來將 ASF 檔案寫入 (QASF) ](building-filter-graphs-to-write-asf-files--qasf.md)           | 描述如何建立檔轉碼和捕獲圖形。                           |
| [ (QASF) 設定設定檔和其他檔案屬性 ](configuring-profiles-and-other-file-properties--qasf.md) | 說明如何使用 WM ASF 寫入器執行各種 ASF 檔案設定工作。 |



 

 

 
