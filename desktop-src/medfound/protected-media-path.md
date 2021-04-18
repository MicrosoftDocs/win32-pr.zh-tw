---
description: 本主題討論三個相互關聯的主題：受保護的環境、媒體互通性閘道，以及撤銷和更新。
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: 受保護的媒體路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104569249"
---
# <a name="protected-media-path"></a>受保護的媒體路徑

本主題討論三個相互關聯的主題：受保護的環境、媒體互通性閘道，以及撤銷和更新。

-   受保護的環境 (PE) 是一組技術，可讓受保護的內容以受保護的方式從 Windows Vista 和 Windows Vista 進行流動。 受保護環境內的所有元件都是受信任的，且程式會受到保護以防止遭到篡改。
-   受保護的媒體路徑 (PMP) 是在受保護的環境中執行的可執行檔。
-   如果 PE 中受信任的元件遭到入侵，則在到期的程式之後，將會予以撤銷。 不過，當有可用的元件時，Microsoft 會提供更新機制來安裝新版的受信任版本。

如需程式碼簽署受保護媒體元件的相關資訊，請參閱 [Windows Vista 中受保護媒體元件的白皮書程式碼簽署](/windows-hardware/test/hlk/)。

本主題包含下列幾節：

-   [受保護的環境](#protected-environment)
-   [受保護環境的設計](#design-of-the-protected-environment)
-   [受保護的媒體路徑](#protected-media-path)
    -   [輸入信任授權單位](#input-trust-authorities)
    -   [輸出信任授權單位](#output-trust-authorities)
    -   [原則物件](#policy-objects)
    -   [在 PMP 中建立物件](#creating-objects-in-the-pmp)
-   [原則協調的總覽](#overview-of-policy-negotiation)
-   [撤銷和續約](#revocation-and-renewal)
-   [輸出連結保護](#output-link-protection)
-   [相關主題](#related-topics)

## <a name="protected-environment"></a>受保護的環境

內容保護包含多項技術，每個技術都會嘗試確保內容的使用方式不會與內容擁有者或提供者的意圖不一致。 這些技術包括禁止複製、連結保護、條件式存取，以及數位版權管理 (DRM) 。 每個信任的基礎是信任：僅授與符合指派給該內容之使用條款的軟體元件的存取權。

為了將受保護內容的威脅降至最低，Windows Vista 和媒體基礎 Software 可讓受信任程式碼在受保護的環境中執行。 PE 是一組元件、指導方針和工具，其設計目的是為了加強對內容盜版的防護。

更仔細地檢查 PE 之前，請務必瞭解它所設計來最小化的威脅。 假設您是在使用者模式進程中執行媒體應用程式。 應用程式會連結至包含媒體外掛程式的各種動態連結程式庫 (Dll) ，例如，解碼器。 其他進程也會在使用者模式下執行，而且會在核心中載入各種驅動程式。 如果沒有信任機制，則會有下列威脅：

-   應用程式可以直接存取受保護的媒體，或攻擊程式記憶體。
-   外掛程式可以直接存取內容，也可以攻擊進程記憶體。
-   其他進程可以直接或藉由插入程式碼，來攻擊媒體程式記憶體。
-   核心驅動程式可以攻擊媒體進程記憶體。
-   內容可能會透過未受保護的媒體在系統外部傳送。  (連結保護的設計目的是要減輕此威脅。 ) 

## <a name="design-of-the-protected-environment"></a>受保護環境的設計

受保護的環境會在與媒體應用程式不同的受保護進程中執行。 Windows Vista 受保護的進程功能會阻止其他進程存取受保護的進程。

建立受保護的進程時，核心核心元件會識別不受信任的元件和外掛程式，讓受保護的環境拒絕載入它們。 受信任的元件是由 Microsoft 適當簽署的元件。 核心也會追蹤載入的模組，如果未受信任的模組載入，則可讓受保護的環境停止播放受保護的內容。 在載入核心元件之前，核心會進行檢查以判斷它是否受信任。 如果不是，則已在 PE 中的受信任元件拒絕處理受保護的內容。 為了啟用此方式，PE 元件會定期執行以密碼編譯保護的信號交換與核心。 如果沒有未受信任的核心模式元件，交握會失敗，並向 PE 指出未受信任的元件存在。

如果信任的元件遭到入侵，則在到期的程式之後，就可以撤銷它。 Microsoft 提供更新機制來安裝較新的受信任版本（如果有的話）。

## <a name="protected-media-path"></a>受保護的媒體路徑

受保護的媒體路徑 (PMP) 是媒體基礎的主要 PE 可執行檔。 PMP 是可擴充的，因此可以支援協力廠商內容保護機制。

PMP 會使用任何內容保護系統（包括由協力廠商提供的），從任何媒體基礎來源接受受保護的內容和相關聯的原則。 只要接收器符合來源所指定的原則，它就會將內容傳送至任何媒體基礎接收。 它也支援來源和接收之間的轉換（包括協力廠商轉換），只要它們是受信任的。

PMP 會在受保護的進程中執行，並與媒體應用程式隔離。 應用程式只能透過 PMP 交換命令和控制訊息，但在傳遞至 PMP 之後，就無法存取內容。 下圖說明此程序。

![受保護媒體路徑的圖表](images/pmp04.png)

陰影方塊代表可能由協力廠商提供的元件。 在受保護的進程內建立的所有元件都必須經過簽署和信任。

應用程式會在受保護的進程內建立媒體會話的實例，並接收 proxy 媒體會話的指標，以封送處理跨進程界限的介面指標。

您可以在應用程式進程（如這裡所示）或受保護的進程內建立媒體來源。 如果媒體來源是在應用程式進程內建立的，則來源會在受保護的進程中建立本身的 proxy。

所有其他的管線元件（例如，解碼器和媒體接收器）都會在受保護的進程中建立。 如果這些物件會公開應用程式的任何自訂介面，則必須提供 DCOM proxy/stub 來封送處理介面。

若要在受保護的內容流經管線時強制執行原則，PMP 會使用三種類型的元件：輸入信任授權單位 (ITAs) 、輸出信任授權單位 (OTAs) 和原則物件。 這些元件會一起運作，以授與或限制使用內容的許可權，並指定在播放內容時必須採用的連結保護，例如高頻寬數位內容保護 (HDCP) 。

### <a name="input-trust-authorities"></a>輸入信任授權單位

ITA 是由受信任的媒體來源所建立，並會執行數個功能：

-   指定使用內容的許可權。 許可權可以包含播放內容、將其傳輸至裝置等的許可權。 它會定義已排序的輸出保護系統清單，以及每個系統的對應輸出原則。 ITA 會將這項資訊儲存在原則物件中。
-   提供解密內容所需的解密子。
-   在受保護的環境中建立與核心模組的信任，以確保 ITA 是在受信任的環境內執行。

ITA 與包含受保護內容的個別資料流程相關聯。 一個串流只能有一個 ITA，而一個 ITA 的實例只能與一個資料流程相關聯。

### <a name="output-trust-authorities"></a>輸出信任授權單位

OTA 與受信任的輸出相關聯。 OTA 會公開受信任的輸出可以在內容上執行的動作，例如播放或複製。 它的角色是強制執行一個或多個由 ITA 所要求的輸出保護系統。 OTA 會查詢 ITA 提供的原則物件，以判斷它必須強制執行的保護系統。

### <a name="policy-objects"></a>原則物件

原則物件會封裝 ITA 的內容保護需求。 原則引擎會使用它來與 OTA 協商內容保護支援。 OTAs 查詢原則物件，以判斷它們必須在目前內容的每個輸出上強制執行的保護系統。

### <a name="creating-objects-in-the-pmp"></a>在 PMP 中建立物件

若要在受保護的媒體路徑中建立物件 (PMP) ， [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 會呼叫 [**IMFPMPHostApp：： ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid)，並以下列方式格式化指定的輸入 **IStream** ：

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>原則協調的總覽

在 PMP 中處理受保護的內容之前，必須符合三個基本需求。 首先，受保護的內容必須只傳送至信任的輸出。 其次，只有允許的動作必須套用至資料流程。 第三，只必須使用已核准的輸出保護系統來播放資料流程。 原則引擎會在 ITAs 和 OTAs 之間協調，以確保符合這些需求。

要瞭解程式最簡單的方式，就是逐步解說簡化的範例，此範例會識別在 Windows Media 數位 Rights Management (WMDRM) 所保護 (ASF) 內容所需的步驟。

當使用者啟動播放程式應用程式，並開啟具有受保護音訊串流和受保護影片串流的 ASF 檔案時，必須執行下列步驟：

1.  應用程式會建立 ASF 媒體來源和受保護的媒體路徑 (PMP) 會話。 媒體基礎會建立 PMP 進程。
2.  應用程式會建立部分拓撲，其中包含連線到音訊轉譯器的音訊來源節點，以及連線至增強型影片轉譯器 (EVR) 的影片來源節點。 在轉譯器中，應用程式不會直接建立轉譯器。 相反地，應用程式會在未受保護的進程中建立稱為 *啟用物件* 的物件。 PMP 使用啟始物件在受保護的進程中建立轉譯器。  (如需啟用物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。 ) 
3.  應用程式會在 PMP 會話上設定部分拓撲。
4.  PMP 會話會將拓撲序列化，並將它傳遞給受保護進程中的 PMP 主機。 PMP 主機會將拓撲傳送至原則引擎。
5.  拓撲載入器會在 ITAs 上呼叫 [**IMFInputTrustAuthority：： GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) ，並將該 decrypters 插入緊接在對應來源節點下游的拓撲中。
6.  拓撲載入器會插入 decrypter 節點下游的音訊和影片解碼器。
7.  原則引擎會掃描插入的節點，以判斷是否有任何可執行檔 [**IMFTrustedOutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) 介面。 EVR 和音訊轉譯器都會執行 **IMFTrustedOutput**，因為它們會將資料傳送到 PMP 外部。
8.  每個 ITA 都確認它是在受保護的進程內執行，方法是使用受保護的環境核心模組來執行密碼編譯交握。
9.  針對每個資料流程，原則引擎會藉由取得來自 ITA 的原則物件，並將它傳遞給 OTA 來協商原則。 OTA 提供它所支援的保護系統清單，而 policy 物件則指出必須套用的保護系統，以及正確的設定。 OTA 接著會套用這些設定。 如果無法這麼做，就會封鎖內容。

## <a name="revocation-and-renewal"></a>撤銷和續約

如果信任的元件遭到入侵，或發現違反其最初受信任的授權合約，便可予以撤銷。 有一項更新機制可安裝較新且更受信任的元件版本。

受信任的元件會使用密碼編譯憑證進行簽署。 Microsoft 會發佈全域撤銷清單 (的 GRL) ，以識別已撤銷的元件。 GRL 經過數位簽署，以確保它的真實性。 內容擁有者可以透過原則機制確保使用者電腦上目前的 GRL 版本存在。

## <a name="output-link-protection"></a>輸出連結保護

當觀看 premium 影片內容時，解密的未壓縮框架會在實體連接器間傳送至顯示裝置。 內容提供者可能需要在此時間點保護影片畫面，因為它們會在實體連接器間移動。 基於此目的，有各種保護機制，包括 High-Bandwidth 數位內容保護 (HDCP) 和 DisplayPort 內容保護 (DPCP) 。 這段影片會使用 [輸出保護管理員](output-protection-manager.md) (OPM) 來強制執行這些保護。 輸出保護管理員會將命令傳送到圖形驅動程式，而圖形驅動程式會強制執行原則所需的任何連結保護機制。

![顯示影片 ota 與 opm 之間關聯性的圖表。](images/pmp05.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> <dt>

[PMP 媒體會話](pmp-media-session.md)
</dt> </dl>

 

 
