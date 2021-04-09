---
description: 下列詞彙有助於瞭解 TAPI 技術。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 36b1d6c3-2d57-4b38-a35f-6bf632411c6e
title: 'T (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 342a27d4ed54458f8645ac5bb49b7ea49baafb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849226"
---
# <a name="t-telephony-api"></a>T (電話語音 API) 

[](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](u-tapgloss.md) [](v-tapgloss.md) [W](w-tapgloss.md) X Y Z

<dl> <dt>

<span id="tapi2.t1_e1_tapgloss"></span><span id="TAPI2.T1_E1_TAPGLOSS"></span>**T1/E1**
</dt> <dd>

容量為 1544 Mbps 的數位傳輸連結。 在美國，此連結稱為 *T1*。 在歐盟，它稱為 *E1*。 請參閱 [*每秒百萬位元 (Mbps)*](m-tapgloss.md)。

</dd> <dt>

<span id="tapi2.tapi_tapgloss"></span><span id="TAPI2.TAPI_TAPGLOSS"></span>**Tapi**
</dt> <dd>

請參閱 *(TAPI) 的電話語音應用程式設計介面*。

</dd> <dt>

<span id="tapi2.tapisrv_tapgloss"></span><span id="TAPI2.TAPISRV_TAPGLOSS"></span>**tapisrv**
</dt> <dd>

支援服務應用程式，提供 TAPI 動態連結程式庫的執行內容，以執行工作，例如配置記憶體或存取已交換至磁片的資料結構。

</dd> <dt>

<span id="tapi2.tdd_tapgloss"></span><span id="TAPI2.TDD_TAPGLOSS"></span>**Tdd**
</dt> <dd>

請參閱 *適用于失聰 (TDD) 的電訊裝置*。

</dd> <dt>

<span id="tapi2.telecommucations_devices_for_the_deaf_tdd__tapgloss"></span><span id="TAPI2.TELECOMMUCATIONS_DEVICES_FOR_THE_DEAF_TDD__TAPGLOSS"></span>**Telecommucations 適用于失聰 (TDD) 的裝置**
</dt> <dd>

用於傳輸編碼信號的資料裝置。 裝置通常是由鍵盤、聲場耦合器和顯示器所組成的簡單電腦終端機，並在300波特執行。

</dd> <dt>

<span id="tapi2.telephony_tapgloss"></span><span id="TAPI2.TELEPHONY_TAPGLOSS"></span>**電話**
</dt> <dd>

使用將電腦與電話網絡整合的技術，以距離傳輸語音、資料、影片或圖像信號的科學。

</dd> <dt>

<span id="tapi2.telephony_application_programming_interface_tapi__tapgloss"></span><span id="TAPI2.TELEPHONY_APPLICATION_PROGRAMMING_INTERFACE_TAPI__TAPGLOSS"></span>**(TAPI) 的電話語音應用程式設計介面**
</dt> <dd>

一組功能，可讓您以與裝置無關的方式來設計以裝置為基礎的裝置，並將個人電話語音提供給使用者。 TAPI 支援語音和資料傳輸、允許各種不同的終端機裝置，並支援複雜的連線類型和通話管理技術，例如會議電話、通話等候和語音信箱。 TAPI 允許所有電話使用的專案，從簡單撥號通話到國際電子郵件，都是在針對 Microsoft Windows 開發的應用程式中控制。 查看 [Microsoft 電話語音總覽](./microsoft-telephony-overview.md)

</dd> <dt>

<span id="tapi2.telephony_service_provider_interface_tspi__tapgloss"></span><span id="TAPI2.TELEPHONY_SERVICE_PROVIDER_INTERFACE_TSPI__TAPGLOSS"></span>**電話語音服務提供者介面 (TSPI)**
</dt> <dd>

用來建立 Microsoft Windows 作業系統服務提供者的工具。 TSPI 會定義網路與 Windows 電話通訊的資訊，進而與 windows 電話語音應用程式溝通的 API 交談。 如需詳細資訊，請參閱 [電話語音服務提供者介面 (TSPI) ](./telephony-service-provider-interface-tspi-.md)。

</dd> <dt>

<span id="tapi2.third_party_call_control_tapgloss"></span><span id="TAPI2.THIRD_PARTY_CALL_CONTROL_TAPGLOSS"></span>**協力廠商呼叫控制**
</dt> <dd>

合作物件呼叫控制模型，可讓應用程式建立或接聽任何雙方的呼叫。

</dd> <dt>

<span id="tapi2.time_to_live_ttl__tapgloss"></span><span id="TAPI2.TIME_TO_LIVE_TTL__TAPGLOSS"></span>**存留時間 (TTL)**
</dt> <dd>

範圍0到255的值，可定義使用網際網路通訊協定 (IP) 在網路上傳送多播封包的範圍。 範圍是根據本機或遠端封包的目的地來定義。 每個路由器都會將 TTL 遞減一。 當值達到預先定義的下限時，路由器會擲回封包。 目前的多播骨幹 (MBONE) 需求，可在 ftp://ftp.isi.edu/mbone/faq.txt 網站取得，請定義下列標準範圍：區域網路、1;本機網站、15;region、63;世界、127。 其他設定可能具有本機意義;例如，31可能表示特定組織內的所有網站。

</dd> <dt>

<span id="tapi2.tspi_tapgloss"></span><span id="TAPI2.TSPI_TAPGLOSS"></span>**TSPI**
</dt> <dd>

請參閱 [電話語音服務提供者介面 (TSPI) ](./telephony-service-provider-interface-tspi-.md)。

</dd> <dt>

<span id="tapi2.ttl_tapgloss"></span><span id="TAPI2.TTL_TAPGLOSS"></span>**Ttl**
</dt> <dd>

查看 *存留時間 (TTL)*。

</dd> <dt>

<span id="tapi2.twisted_pair_tapgloss"></span><span id="TAPI2.TWISTED_PAIR_TAPGLOSS"></span>**雙絞線配對**
</dt> <dd>

一般的電話線路。 每個電話線實際上都是一對電線。

</dd> </dl>

 

 
