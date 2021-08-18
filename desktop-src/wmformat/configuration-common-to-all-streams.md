---
title: 所有資料流程通用的設定
description: 所有資料流程通用的設定
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- 設定檔，所有資料流程通用的設定
- 資料流程，一般設定
- 資料流程，名稱
- 資料流程，連接名稱
- 資料流程、數位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e8b58e97ce2add4b6ff139aebacbc6d510af4424b2d3ae2bff3ea4577c429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964177"
---
# <a name="configuration-common-to-all-streams"></a>所有資料流程通用的設定

無論何種類型，所有的資料流程都應該指派資料流程名稱、連接名稱和資料流程號碼。

資料流程名稱只是您指派給資料流程的描述性名稱。 資料流程不需要有資料流程名稱，但它可在稍後編輯設定檔時，協助您識別該資料流程。 您可以藉由呼叫 [**IWMStreamConfig：： SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname)來設定資料流程的名稱。

每個資料流程都應該有連接名稱，也稱為輸入名稱。 當您將寫入器物件中的設定檔設定為寫入檔案時，寫入器會將每個連接名稱與輸入產生關聯。 若要識別輸入，您必須呼叫 [**IWMInputMediaProps：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) 來取出連接名稱。 一般連接名稱是內容的簡單描述，例如「音訊」。 如果您的設定檔包含以位元速率互斥的資料流程，每個互斥資料流程都必須有相同的連接名稱。 如果不是，則設定檔無效，寫入器將會拒絕此設定檔。 您可以藉由呼叫 [**IWMStreamConfig：： SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname)來設定連接名稱。

資料流程號碼會識別檔案內的資料流程。 不同于輸入編號和輸出編號，資料流程號碼從1開始，而不是0。 資料流程號碼與資料流程索引不同，您在使用 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)取得設定檔中的資料流程時，會使用此索引。 資料流程索引是由設定檔物件指派給資料流程的數位。 資料流程索引的範圍介於0到1之間，且小於 [**IWMProfile：： GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount)所抓取的資料流程數目。 資料流程號碼不需要是連續的，但它們通常都是，而且範圍可以從1到63。 您可以藉由呼叫 [**IWMStreamConfig：： SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber)來設定串流號碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




