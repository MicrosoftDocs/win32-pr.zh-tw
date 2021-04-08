---
title: 將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10
description: 將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK，轉換受 DRM 保護的檔案
- Windows Media Format SDK，受 DRM 保護的檔案
- Advanced Systems Format (ASF) ，轉換受 DRM 保護的檔案
- ASF (Advanced Systems 格式) ，轉換受 DRM 保護的檔案
- Advanced Systems Format (ASF) 、受 DRM 保護的檔案
- ASF (Advanced Systems Format) 、受 DRM 保護的檔案
- 數位版權管理 (DRM) ，轉換受 DRM 保護的檔案
- DRM (數位版權管理) ，轉換受 DRM 保護的檔案
- 數位版權管理 (DRM) 、受 DRM 保護的檔案
- DRM (數位版權管理) 、受 DRM 保護的檔案
- Windows Media Format SDK，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Windows Media Format SDK、DRM 10
- Advanced Systems Format (ASF) 、適用于網路裝置的 Windows Media DRM 10
- ASF (Advanced Systems Format) ，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Advanced Systems Format (ASF) ，DRM 10
- ASF (Advanced Systems Format) ，DRM 10 用於網路裝置
- 數位版權管理 (DRM) ，適用于網路裝置的 Windows Media DRM 10
- DRM (數位版權管理) 、適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的數位版權管理 (DRM) ，DRM 10
- DRM (數位版權管理) ，DRM 10 用於網路裝置
- 適用于網路裝置的 Windows Media DRM 10，轉換受 DRM 保護的檔案
- 適用于網路裝置的 DRM 10，轉換受 DRM 保護的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644c1b4f7ede688434fbb1dde11b7051c6f644a5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681434"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10

註冊並驗證裝置之後，您就可以開始處理授權要求訊息。 當需要應用程式的動作時，裝置會傳送授權要求訊息。 目前唯一支援的動作是「播放」，這是保護資料以進行播放的要求。

當您收到授權要求訊息時，您應該執行下列步驟：

1.  藉由呼叫 [**IWMDRMMessageParser：:P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) 方法來剖析授權要求訊息。
2.  藉由呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid)方法，並傳入步驟1中取得的憑證和序號，來取得裝置的 [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)介面。
3.  確認裝置已準備好接收安全資料：
    -   呼叫 [**IWMRegisteredDevice：： IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) 確認裝置是否已通過核准。 核准應一律以使用者喜好設定為基礎。
    -   呼叫 [**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) 來確認裝置已在過去48小時內經過驗證。 如果裝置無效，您需要執行鄰近性偵測。 如需詳細資訊，請參閱 [執行鄰近性偵測](performing-proximity-detection.md)。
    -   呼叫 [**IWMRegisteredDevice：： IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) 來確認裝置已開啟。 如果裝置未開啟，您可以藉由呼叫 [**IWMRegisteredDevice：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)來開啟它。 您一次只能在電腦上開啟10部裝置。 您可能需要關閉其他裝置，才能開啟您要處理要求的裝置。 若要關閉裝置，請呼叫 [**IWMRegisteredDevice：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) 方法。
4.  藉由呼叫 [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) 函數來建立 DRM transcryptor 物件的實例。
5.  呼叫 [**IWMDRMTranscryptor：： initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) 方法以初始化 transcryptor。 這個方法會採用 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的指標，它會用來傳遞狀態訊息。 此方法也會傳回必須傳送給裝置的授權要求訊息，然後再繼續。
6.  當您的應用程式 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法收到 WMT \_ TRANSCRYPTOR \_ INIT 狀態訊息時，請呼叫 [**IWMDRMTranscryptor：： seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) 方法來搜尋檔案中的適當開始位置。 若要從檔案的開頭開始，您必須使用時間0呼叫 **Seek** 。
7.  \_ \_ 當 transcryptor 已準備好在新的呈現時間從檔案傳遞資料時，會傳送 WMT transcryptor SEEKED 訊息。 對 [**IWMDRMTranscryptor：： Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) 方法進行重複呼叫，以取得轉換的媒體資料區塊。 每個呼叫都是非同步，而且在接收到 WMT \_ TRANSCRYPTOR READ 訊息之前都不會完成 \_ 。 當您收到訊息時，可以將資料傳送至接收裝置。
8.  當您收到 WMT \_ TRANSCRYPTOR \_ READ 訊息，並將 *hr* 參數設定為 NS \_ S \_ TRANSCRYPTOR EOF 時，就會 \_ 讀取整個檔案。 此時，請呼叫 [**IWMDRMTranscryptor：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) 方法來關閉檔案和釋放資源。
9.  當收到 WMT \_ TRANSCRYPTOR \_ 已關閉的訊息時，您可以釋放 [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) 介面。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 Windows Media DRM 10 進行網路裝置通訊協定**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




