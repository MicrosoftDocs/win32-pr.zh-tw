---
title: 從編解碼器取得串流設定資訊
description: 從編解碼器取得串流設定資訊
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- 串流，來自編解碼器的設定
- 編解碼器，取得串流設定
- 資料流程、編解碼器格式
- 編解碼器，格式
- 資料流程，IWMCodecInfo 介面
- IWMCodecInfo，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104374769"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>從編解碼器取得串流設定資訊

針對使用 Windows Media 音訊和影片編解碼器的音訊和影片串流，您應該從您想要使用的編解碼器取得串流設定結構的值。 雖然您可以自行設定這些值，但使用編解碼器可確保這些值是正確的。 除非檔特別建議特定的變更，否則您不應該改變這些結構中的值。

編解碼器的資訊採用編解碼器格式的形式。 每個編解碼器格式都是編解碼器支援的單一資料流程格式。 如需資料流程格式的詳細資訊，請參閱 [格式](formats.md)。

您可以使用配置檔案管理員物件的 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)、 [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)和 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 介面，從 Windows Media 編解碼器要求資訊。 若要取得配置檔案管理員物件的 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面，請呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數。 在 **IWMProfileManager** 上呼叫 **QueryInterface** 以取得 **IWMCodecInfo3**。

下列各節將說明如何取得您需要的資訊。



| 區段                                                                                                | 描述                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [列舉所有已安裝的 Windows Media 編解碼器](to-enumerate-all-installed-windows-media-codecs.md) | 說明如何使用 **IWMCodecInfo** 和 **IWMCodecInfo2** 介面的方法，以抓取每個已安裝 Windows Media 編解碼器的名稱和編解碼器索引。 |
| [列舉編解碼器格式](to-enumerate-codec-formats.md)                                           | 說明如何從編解碼器取得串流設定物件，以便在您的設定檔中使用。                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> </dl>

 

 




