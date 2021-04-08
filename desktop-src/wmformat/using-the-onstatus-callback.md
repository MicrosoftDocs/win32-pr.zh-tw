---
title: 使用 OnStatus 回呼
description: 使用 OnStatus 回呼
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK，OnStatus 回呼方法
- Windows Media Format SDK，IWMStatusCallback 介面
- OnStatus 回呼方法，關於
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932910"
---
# <a name="using-the-onstatus-callback"></a>使用 OnStatus 回呼

Windows Media 格式 SDK 中的數個物件會呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法。 **OnStatus** 會接收表示 SDK 作業狀態變更的訊息。

若要使用 **OnStatus** 回呼方法，您必須在應用程式中執行繼承自 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的類別。 在類別中包含 **OnStatus** 版本的程式碼。 您可以在此 SDK 隨附的範例中找到數個 **OnStatus** 的範例。 如需範例的詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

您必須將狀態回呼的執行與 Windows Media Format SDK 的各種物件產生關聯。 每個物件都有不同的方式來建立此關聯。 如需關聯特定物件的方法清單，請參閱 **IWMStatusCallback** 參考頁面。

**OnStatus** 可接收的狀態訊息是在 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)列舉類型中定義。

您可以選擇要設陷的訊息，以及要忽略的訊息。 不過，某些功能需要回應某些狀態訊息。 例如，使用非同步讀取器時， [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法會以非同步方式開啟檔案。 要知道檔案何時開啟的唯一方法，就是將 MWT-DS 開啟的訊息設為陷阱 \_ 。 一般來說，您回應的訊息是非同步工作完成的通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用回呼方法**](using-the-callback-methods.md)
</dt> </dl>

 

 




