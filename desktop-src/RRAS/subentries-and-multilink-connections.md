---
title: 子機和多重連結連接
description: Windows NT Server 4.0 支援電話簿子機，可啟用多重連接連線。 多重連接連接會結合多個連線的頻寬，以提供具有更高頻寬的單一連線。
ms.assetid: 19cf6e1a-cdba-47e4-8d8f-d6030ed6f9e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1970e2e2ad668b376b1097aa20cd18986fb605a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316078"
---
# <a name="subentries-and-multilink-connections"></a>子機和多重連結連接

Windows NT Server 4.0 支援電話簿子機，可啟用多重連接連線。 多重連接連接會結合多個連線的頻寬，以提供具有更高頻寬的單一連線。

RAS 電話簿專案可以有零或多個子專案。 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)函式會抓取 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))結構，其中包含有關電話簿專案之子專案的資訊。 **RASENTRY** 結構的 **dwSubEntries** 成員會指出子值的數目。 電話簿一開始沒有任何子專案。 若要將子專案新增至電話簿專案，請使用 [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) 函數。

每個子索引的屬性都包含電話號碼，以及撥號裝置的撥號時所要使用之 TAPI 裝置的名稱和類型。 此外，如果 RAS 無法使用主要號碼進行連線，則子索引可包含備用電話號碼清單來撥打電話。 [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)和 [**RasGetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa)函式會使用 [**RASSUBENTRY**](/previous-versions/windows/desktop/legacy/aa377839(v=vs.85))結構來設定和取出指定的電話通訊錄子索引項目的屬性。 子索引是以以一個為基礎的索引來識別。

您可以呼叫 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函式來設定多重連結 RAS 專案，以在第一次撥號時連接所有的子機。 或者，您可以設定專案以提供可變頻寬。 在此情況下，RAS 一開始會連接單一子索引，然後視需要連接或中斷連接其他子服務。 若為可變頻寬的多重連結連接，您可以使用 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) 結構來指定當您呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式時要連接的初始子索引。 使用 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) 函式來連接多重連結專案時，您可以使用 [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) 結構來指定要連接的初始子索引。

若為可變頻寬的多重連結連接，請使用 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) 結構搭配 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函式來指定連接和中斷個別子機的參數。 當使用的頻寬超過指定間隔的可用頻寬指定百分比時，RAS 會連接額外的子索引。

如果您呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式來建立多重連結連接，您可以指定 [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) 回呼函式來接收有關連接的通知。 **RasDialFunc2** 類似于 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) 回呼函式，不同之處在于它會提供多重連結連接的額外資訊，例如造成通知的子索引。 當 RAS 連線或中斷連接子索引的連線時，會呼叫您的 **RasDialFunc2** 函式。

您可以使用 **HRASCONN** 連接控制碼來掛上或取得多重連結連接的相關資訊。 您可以針對組成多重連結的每個子索引連接，以及合併的多重連結連接，取得連接控制碼。 當您呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式來建立多重連結連接時， **RasDial** 會將控制碼傳回至合併的多重連結連接。 同樣地，當您列舉連接時， [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) 會傳回合並的多重連結控制碼。 若要取得多重連結連接中其中一個子索引連接的控制碼，請呼叫 [**RasGetSubEntryHandle**](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea) 函數。

您可以在 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)、 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)和 [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) 函式中使用合併的多重連結連接控制碼和子索引連接控制碼。 使用合併的多重連結控制碼呼叫 **RasHangUp** 會終止整個連接;使用子索引介面進行呼叫，只會使該子索引的連線停止回應。 同樣地， **RasGetConnectStatus** 會根據指定的控制碼，傳回合並或個別連接的資訊。 **RasGetProjectionInfo** 針對多重連接專案所傳回的投射資訊，對於主要連接控制碼而言是相同的。

 

 