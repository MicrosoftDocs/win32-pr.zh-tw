---
description: 設定 ASF 分隔器物件
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: 設定 ASF 分隔器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f27885e602dd52012808d330d997f9b7a7e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111841"
---
# <a name="configuring-the-asf-splitter-object"></a>設定 ASF 分隔器物件

ASF *分隔器* 物件是 WMContainer 層物件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。 建立並初始化分隔器來剖析媒體檔案的 ASF 資料物件之後，必須設定分隔器，以產生特定資料流程的範例。 呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) 來選取所需的資料流程。

或者，應用程式也可以將它設定為以反向順序產生範例，或產生受保護內容的範例。 若要設定這些選項，請呼叫 [**IMFASFSplitter：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) ，並傳遞所支援旗標所需的位組合。 在呼叫這個方法之前，用戶端必須成功完成 [**IMFASFSplitter：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 呼叫;否則， **SetFlags** 會失敗，並出現 **MF \_ E \_ 未 \_ 初始化** 的錯誤碼。 如需初始化分隔器的詳細資訊，請參閱 [建立 ASF 分隔器物件](creating-the-asf-splitter-object.md)。

若要檢查此旗標目前是否已在分隔器上設定，請呼叫 [**IMFASFSplitter：： GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags)。

## <a name="selecting-streams-for-parsing"></a>選取要剖析的資料流程

在初始化過程中，透過 [**IMFASFSplitter：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 呼叫，分割器會偵測 ASF 檔案中的資料流程數目和資料流程識別碼。 依預設，分隔器不會選取任何資料流程。 應用程式必須藉由呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)來選取資料流程。 這個方法會接受資料流程編號的陣列。 若要取得資料流程的資料流程號碼，請在 ASF 設定檔上呼叫 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) ，或在資料流程描述項上呼叫 [**IMFStreamDescriptor：： GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) 。  (您可以從 ContentInfo 物件取得 ASF 設定檔和串流描述項。 ) 如果用戶端傳遞的資料流程號碼無法由分隔器辨識，則會因為 **MF \_ E \_ INVALIDSTREAMNUMBER** 錯誤而失敗。

呼叫 [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) 會清除先前的選取專案。 未選取任何未在陣列中指定的資料流程。 若要取得目前選取的資料流程清單，請呼叫 [**IMFASFSplitter：： GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams)。 這個方法會採用陣列的指標，此方法會以資料流程號碼填滿。 如果陣列大小小於所選資料流程的數目，則方法會因 **MF \_ E \_ BUFFERTOOSMALL** 錯誤而失敗。 在此情況下，方法會傳回 *pwNumStreams* 參數中選取的資料流程數目。 然後，您可以使用此數位來配置正確大小的陣列，並再次呼叫方法。

如需範例程式碼，請參閱 [教學課程：讀取 ASF](tutorial--reading-an-asf-file.md)檔案中的「選取要剖析的資料流程」。

## <a name="reverse-playback-setting"></a>反向播放設定

在分隔器的初始化程式中，它會判斷 ASF 內容是否支援反向播放。 如果有的話，就可以設定 **MFASF \_ 分隔器 \_ 反向** 旗標，將分隔器設定為以反向順序產生樣本。 如果內容不支援反向播放， [**IMFASFSplitter：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) 會傳回 **MF \_ E \_ INVALIDREQUEST**，但是會在分隔器上設定旗標。

如果分隔器已設定為以反向方向進行剖析，則分隔器一律會在包含 ASF 資料物件之緩衝區的結尾處開始剖析。 因此，若要對資料位移進行反向剖析，以及要剖析的資料長度必須適當地設定。 如需設定正確值的詳細資訊，請參閱 [從現有的 ASF 資料物件產生資料流程範例](generating-stream-samples-from-an-existing-asf-data-object.md)。

## <a name="protected-content-setting"></a>受保護的內容設定

您可以設定 **MFASF \_ 分隔器 \_ WMDRM** 至 [**IMFASFSplitter：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags)，將分隔器設定為使用封包層級的加密內容。 這會指示分隔器提供 Windows Media 數位 Rights Management (DRM) 所保護之內容的範例。 當設定這個旗標時，分隔器所產生的範例會包含解密媒體資料和重建框架所需的資訊，例如 [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md) 屬性。 這個屬性是包含 **DWORD** s 陣列的 blob。 每個 **DWORD** 都會針對框架提供相對於框架開頭的承載界限。 如果這個屬性不存在，則框架會包含在單一承載中。 一般而言，分隔器所產生的範例包含多個媒體緩衝區，應用程式可以呼叫 [**IMFSample：： ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)，將所有緩衝區複製到一個連續的緩衝區。 產生的緩衝區包含框架，而屬性值則包含這個緩衝區的位移。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 分隔器](asf-splitter.md)
</dt> </dl>

 

 



