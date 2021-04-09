---
title: 將 ASF 資料傳送至發行端點
description: 將 ASF 資料傳送至發行端點
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK，傳送 ASF 資料
- Windows Media Format SDK，發行端點
- Advanced Systems Format (ASF) ，傳送資料
- ASF (Advanced Systems Format) ，傳送資料
- Advanced Systems Format (ASF) 、發行端點
- ASF (Advanced Systems Format) ，發行端點
- 發行端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681564"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>將 ASF 資料傳送至發行端點

您可以使用 Windows Media Format SDK 將 ASF 資料推送至 Windows Media 伺服器上的發行端點。 然後伺服器會從該發行端點廣播資料。 如果您要在一部電腦上捕獲或重新編碼內容，而且想要從另一部電腦 (或數部電腦) 發佈內容，此案例就很有用。 如果您需要將內容從防火牆內的電腦移至防火牆外部的 Windows Media 伺服器，這也很有用，因為推送散發會使用 HTTP 通訊協定。

> [!Note]  
> *發行端點* 的運作方式基本上就像是重新導向器。 用戶端會在 URL 中指定發行端點 (例如 mms://MyServer/MyPublishingPoint) ，而伺服器會將此內容轉譯成內容的要求。

 

若要將資料推送至發行端點，請將推送接收物件附加至寫入器物件。 推播接收可用來開啟與伺服器的連線，以及管理推播會話。 寫入器物件會處理建立檔案的所有其他層面。

執行下列步驟：

1.  藉由呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函式來建立寫入器物件，該函式會傳回 [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) 指標。
2.  藉由呼叫 [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) 函式來建立推送接收物件，該函式會傳回 [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) 指標。
3.  在寫入器上呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) ，並使用網路接收器的 **IWMWriterPushSink** 介面指標，以將網路接收器附加至寫入器。
4.  藉由呼叫 [**IWMWriterPushSink：： connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect)來連接到伺服器。
5.  寫入資料流。 此步驟包含在寫入器物件上設定設定檔、將範例傳送至寫入器，以及可能的其他工作。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。 其他工作可能包括設定中繼資料屬性 (如 [使用中繼資料](working-with-metadata.md)) 中所述，或在資料流程上設定即時 DRM (如 [啟用 DRM 支援](enabling-drm-support.md)) 所述。 這些工作的執行方式與寫入 ASF 檔案的方式完全相同。
6.  撰寫完成之後，請在寫入器上呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) ，以卸離推送接收物件。
7.  在推播接收上呼叫 [**IWMWriterPushSink：： EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) ，以結束與伺服器的會話。

這些步驟說明于 WMVNetWrite 範例應用程式中。

> [!Note]  
> 如果您要傳送非常低位的僅限影片檔案，它可能不會在發行端點上開始播放幾秒鐘的時間。 這種情況可能會在各種情況下發生，例如，當單一封包包含許多小型影片框架且沒有音訊，或第一個封包與低位視頻檔案中的第二個封包之間有很長的時間間距時。 若要避免這個問題，請在檔案中插入無訊息音訊串流。

 

## <a name="authentication"></a>驗證

推播接收物件會自動處理伺服器的驗證。 不過，應用程式可能需要提供認證。 這是透過 **IWMCredentialCallback** 回呼介面完成的，如下所示：

1.  在您的應用程式中執行 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 和 [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) 介面。
2.  查詢 [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) 介面的推送接收物件。
3.  使用應用程式的 **IWMStatusCallback** 介面指標呼叫 [**IWMRegisterCallback：： Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) 。
4.  如果推送接收需要從應用程式取得認證，它會查詢 **IWMCredentialCallback** 介面的 **IWMStatusCallback** 指標，並呼叫 [**IWMCredentialCallback：： AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials)。 如需此方法的詳細資訊，請參閱 [驗證](authentication.md)。
5.  當您完成時，請呼叫 [**IWMRegisterCallback：： Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) ，以停止從推播接收取得事件通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**透過網路傳送 ASF 資料**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> <dt>

[**寫入器推送接收物件**](writer-push-sink-object.md)
</dt> </dl>

 

 




