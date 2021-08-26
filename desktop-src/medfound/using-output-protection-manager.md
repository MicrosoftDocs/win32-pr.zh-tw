---
description: 深入瞭解：使用輸出保護管理員
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: 使用輸出保護管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e37dd548603a6f9d7769a9e724df3477e2fcde
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475514"
---
# <a name="using-output-protection-manager"></a>使用輸出保護管理員

本主題說明如何使用輸出保護管理員 (OPM) ，以在透過實體連接器傳送至顯示裝置時保護影片內容。 本主題包含下列幾節：

-   [影片輸出](#video-outputs)
-   [將 OPM 會話初始化](#initializing-an-opm-session)
-   [傳送 OPM 狀態要求](#sending-opm-status-requests)
-   [傳送 OPM 命令](#sending-opm-commands)
-   [處理已停用的影片輸出](#sending-opm-commands)
-   [使用 HDCP 來保護內容](#using-hdcp-to-protect-content)

進階版的影片內容通常會經過加密，以防止未經授權的重複。 當然，影片必須先解密才能顯示。 經過解密的未壓縮框架之後，必須傳送至顯示裝置的實體連接器。 內容提供者可能需要在此時間點保護影片畫面，因為它們會在實體連接器間移動。

基於此目的，有各種保護機制，包括 High-Bandwidth 數位內容保護 (HDCP) 和 DisplayPort 內容保護針對數位輸出 (DPCP) ;和複製世代管理系統-類比 (CGMS-類比輸出的) 。 一般而言，這些機制牽涉到加密或編碼 befores 送到顯示器的信號。

OPM 可讓應用程式在影片輸出上強制執行內容保護機制。 使用 OPM 時，應用程式會透過受信任的安全通道，將命令和狀態要求傳送到圖形驅動程式。 OPM 可讓應用程式：

-   確認圖形驅動程式已由 Microsoft 簽署。
-   使用驅動程式設定受信任的通道。
-   在實體輸出上強制執行內容保護機制。

OPM 會將認證的輸出保護協定 (COPP) ，並使用類似的 API。 為了與舊版相容，OPM 介面可以模擬 COPP 介面。 OPM 和 COPP 之間的差異包括下列各項：

-   OPM 會使用 x.509 憑證，而 COPP 會使用專屬的憑證格式。
-   OPM 支援 HDCP 中繼器。
-   使用 OPM 的應用程式不需要剖析 (SRMs) 的 HDCP 系統 renewability 訊息。
-   當圖形顯示使用複製模式時，可以使用 OPM。 COPP 不支援複製模式。

如果您的應用程式使用受保護的媒體路徑 (PMP) 播放影片內容，則不需要使用 OPM API，因為 PMP 會進行所有必要的 OPM 呼叫。 OPM API 適用于未使用 PMP 的應用程式。

OPM 可在 Windows Vista 和更新版本中使用，但在 Windows 7 之前，API 不是公用的。 若要在應用程式中使用 OPM，您必須有 Windows 7 SDK 的標頭和程式庫檔案。 您不需要轉散發任何 dll 以使用 Windows Vista 或 Windows Server 2008 中的 OPM。

## <a name="video-outputs"></a>影片輸出

圖形介面卡可以有一個以上的實體輸出，每個都有自己的功能。 在應用程式播放受保護的內容之前，它必須在與將顯示影片的圖形配接器相關聯的每個影片輸出上設定適當的保護機制。 要套用的保護機制將取決於內容的使用規則。

每個影片輸出都會以 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面的實例來表示。 您可以使用 Direct3D 裝置或監視器控點來取得影片輸出。

使用 Direct3D 裝置：

1.  取得 Direct3D 裝置的 **IDirect3DDevice9** 指標，您的應用程式將使用它來建立用來儲存影片畫面的介面。
2.  呼叫 [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) 函數。 此函式會配置一個 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標的陣列，每個輸出各一個陣列。

使用監視器控制碼：

1.  呼叫 **EnumDisplayMonitors** 以取得對應于影片視窗的 **HMONITOR** 控點。 數個監視器可以與相同的視窗相關聯，因此您可能會收到數個 **HMONITOR** 控制碼。
2.  針對每個監視控制碼，呼叫 [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)。 此函式會配置一個 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標的陣列，每個輸出各一個陣列。

## <a name="initializing-an-opm-session"></a>將 OPM 會話初始化

在應用程式傳送 OPM 命令或狀態要求之前，它必須先確認影片輸出是否受信任，並建立工作階段金鑰。 工作階段金鑰是用來簽署應用程式與圖形驅動程式之間交換的資料。

OPM API 會定義建立信任的交握，並設定工作階段金鑰。 您必須針對每個的 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面實例執行此交握，如下所示：

1.  呼叫 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization)。 這個方法會抓取兩個數據片段：
    -   由驅動程式產生的亂數字。 您將使用此數位來完成交握。
    -   驅動程式的 x.509 憑證鏈。
2.  確認憑證鏈是否已由 Microsoft 簽署。
    > [!Note]  
    > 憑證撤銷超出 OPM 的範圍。

     

3.  從憑證鏈取得驅動程式的公開金鑰。
4.  產生128位 AES 工作階段金鑰。
5.  產生兩個隨機的32位數位：

    -   OPM 狀態要求的起始序號。
    -   OPM 命令的起始序號。

    這些數位必須使用以密碼編譯的安全虛擬亂數產生器（例如 **CryptGenRandom**）來產生。

6.  將步驟 1) 、工作階段金鑰和兩個序號中取得的驅動程式隨機 (數位複製到 [**OPM \_ 加密的 \_ 初始化 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) 結構中，如 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)中所述。
7.  使用驅動程式的公開金鑰（可在驅動程式憑證中找到），以 RSAES-PKCS1-OAEP 加密 [**OPM \_ 加密的 \_ 初始化 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) 結構。
8.  呼叫 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)。

## <a name="sending-opm-status-requests"></a>傳送 OPM 狀態要求

OPM 狀態要求會傳回影片輸出的相關資訊，例如實體連接器的類型和目前的保護層級。 如需要求類型的清單，請參閱 [OPM 狀態要求](opm-status-requests.md)。

若要傳送狀態要求，請執行下列步驟。

1.  初始化 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) 結構，如下表所示。

    | member               | 描述                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**             | 請立即略過此欄位。                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | 密碼編譯安全的128位亂數字。 當您提出狀態要求時，一律會產生新的亂數字，即使您正在進行相同的要求也一樣。 將數位儲存在變數中，因為您稍後將需要參考它。                                                                                                                             |
    | **guidInformation**  | 識別狀態要求的 GUID。 如需狀態要求的清單，請參閱 [OPM 狀態要求](opm-status-requests.md)。                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | 序號。 針對第一個狀態要求，請使用您在 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) 方法中指定的起始序號， ([初始化 OPM 會話](#initializing-an-opm-session)的步驟5。 ) 每次您提出另一個狀態要求時，請將此數位遞增1。 |
    | **abParameters**     | 位元組陣列，其中包含要求的其他輸入資料。 輸入資料的格式會列在每個狀態要求的參考主題中。                                                                                                                                                                                                                    |
    | **cbParametersSize** | **AbParameters** 陣列中的有效資料大小。 陣列其餘部分的內容是未定義的。                                                                                                                                                                                                                                                              |

    

     

2.  計算單鍵 CBC MAC (OMAC-1) 計算 **OMAC** 成員後面出現之資料區塊的雜湊，然後將 **OMAC** 成員設定為此值。 請參閱 [OPM 範例程式碼](opm-example-code.md)。
3.  呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法。 傳入 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) 結構的指標，以及指向 [**OPM \_ 所要求之 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) 結構的指標。 驅動程式的回應會寫入 **OPM 要求的 \_ \_ 資訊** 結構。
    -   此結構的 **omac** 成員包含針對這個成員之後的資料所計算的 omac。
    -   **AbRequestedInformation** 成員是位元組陣列，其中包含回應的輸出資料。 輸出資料的格式會列在每個狀態要求的參考主題中。
4.  計算 [**OPM \_ 所要求 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) 結構的 OMAC，不包含 **OMAC** 成員。 確認 OMAC 與 **OMAC** 成員中的值相符。
5.  請確定 [**OPM 所 \_ 要求的 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構的 **cbRequestedInformationSize** 成員會提供正確的輸出資料大小。 例如， [**OPM \_ GET \_ CONNECTOR \_ 類型**](opm-get-connector-type.md) 查詢的輸出資料是 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) 結構，因此 **cbRequestedInformationSize** 的值應為 `sizeof(OPM_STANDARD_INFORMATION)` 。
6.  將 [**OPM \_ 要求之 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構的 **abRequestedInformation** 成員轉換成正確的輸出資料結構。 例如，如果狀態要求是 [**OPM \_ GET \_ CONNECTOR \_ TYPE**](opm-get-connector-type.md)，請將 **abRequestedInformation** 轉換為 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) 結構。
7.  請確定輸出資料結構的 **rnRandomNumber** 成員符合步驟1中的 **rnRandomNumber** 值。
8.  檢查輸出資料結構的 **ulStatusFlags** 成員，如 [處理已停用的影片輸出](#handling-a-disabled-video-output)中所述。

如果步驟5–8中的任何檢查失敗，應用程式就必須停止顯示受保護的內容。

## <a name="sending-opm-commands"></a>傳送 OPM 命令

OPM 命令是用來設定影片輸出的保護層級和其他設定。 傳送 OPM 命令類似于傳送狀態要求，但驅動程式沒有回應資料。 如需命令清單，請參閱 [OPM 命令](opm-commands.md)。

若要傳送 OPM 命令，請執行下列步驟。

1.  填寫 [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) 結構，如下表所示。

    | member                | 描述                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | 請立即略過此欄位。                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | 識別命令的 GUID。 如需命令清單，請參閱 [OPM 命令](opm-commands.md)。                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | 序號。 若為第一個命令，請使用您在 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) 方法中指定的起始序號， ([初始化 OPM 會話](#initializing-an-opm-session)的步驟5。 ) 每次傳送其他命令時，請將此數位遞增1。 |
    | **abParameters**      | 位元組陣列，其中包含命令的其他輸入資料。 輸入資料的格式會列在每個命令的參考主題中。                                                                                                                                                                                                             |
    | **cbSettingDataSize** | **AbParameters** 陣列中的有效資料大小。 陣列其餘部分的內容是未定義的。                                                                                                                                                                                                                                                |

    

     

2.  計算 **OMAC** 成員後面出現之資料區塊的 OMAC，然後將 **OMAC** 成員設定為此值。
3.  呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)。

大部分的命令都有對應的狀態要求，會傳回命令的狀態。 例如， [**OPM \_ SET \_ 保護 \_ 等級**](opm-set-protection-level.md) 命令會設定保護層級，而 [**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級**](opm-get-virtual-protection-level.md) 命令會取得目前的保護層級。

## <a name="handling-a-disabled-video-output"></a>處理已停用的影片輸出

影片輸出可能會隨時停用，以防止未經授權使用影片內容。 發生這種情況的原因可能是因為驅動程式偵測到篡改，或因為顯示已與實體連接器中斷連線，而導致保護機制停止運作。 當影片輸出停用時，不會顯示任何影片畫面。

在啟用內容保護的情況下，應用程式應該每2秒定期至少 (一次) 執行下列步驟。

1.  呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 以傳送 [**OPM \_ 取得實際的 \_ \_ 保護 \_ 層級**](opm-get-actual-protection-level.md) ，或 [**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 等級**](opm-get-virtual-protection-level.md) 的狀態要求。 這兩個命令的傳回資料是 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) 結構。
2.  檢查 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員。 此成員包含旗標，指出是否仍啟用內容保護。 如果內容保護已關閉，請立即停止播放影片。
3.  如果開啟內容保護，請檢查 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulStatusFlags** 成員。 如果未設定任何旗標，則影片輸出會正常運作。 否則，會停用影片輸出。

下列旗標是針對 **ulStatusFlags** 所定義。




| 旗標 | 描述 | 
|------|-------------|
| <strong>OPM_STATUS_LINK_LOST</strong> | 輸出保護因某些原因而停止運作;例如，顯示裝置可能會從 conntector 中拔下。 停止播放並關閉所有輸出保護機制。 | 
| <strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong> | 應用程式必須重新建立 OPM 會話。 回應方式如下：<ol><li>停止播放。</li><li>關閉所有保護機制。</li><li>釋放 <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> 介面。</li><li>重新建立所有的影片表面。</li><li>建立新的 OPM 物件，並嘗試重新建立內容保護。 如果失敗，則會向使用者顯示錯誤訊息。 請勿播放任何其他的影片內容。</li></ol> | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | 此旗標只適用于使用 HDCP 時，並表示已撤銷的 HDCP 裝置是否存在。 停止播放並關閉此影片輸出上的所有保護機制。 當設定這個旗標時，也會設定 <strong>OPM_STATUS_LINK_LOST</strong> 旗標。 | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | 驅動程式偵測到篡改。 停止播放，並使用此影片輸出播放其他影片。 停止使用任何其他影片輸出也是不錯的主意，因為系統可能會受到危害。 | 




 

## <a name="using-hdcp-to-protect-content"></a>使用 HDCP 來保護內容

本節說明如何使用 OPM 啟用 HDCP 輸出保護。 以下是應用程式必須採取之步驟的一般大綱。 本節稍後會提供詳細資料。

1.  應用程式可能必須將「SRM」提供給影片輸出。 接收 SRMs 的機制在 OPM 介面的範圍之外。 例如，SRMs 可能會作為廣播串流的一部分來傳遞。
2.  應用程式會啟用 HDCP 輸出保護。
3.  應用程式會播放影片內容。 應用程式會定期輪詢驅動程式，以確定 HDCP 已開啟。
4.  播放完成時，應用程式會關閉 HDCP。

### <a name="setting-the-srm"></a>設定 SRM

若要設定 SRM，請執行下列步驟。

1.  使用 SRM 版本號碼，初始化 [**OPM \_ SET \_ HDCP \_ SRM \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) 結構。
2.  將 SRM 儲存在變數中。
3.  將 [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令傳送到影片輸出。 使用傳送 [OPM 命令](#sending-opm-commands)中所述的程式。
    -   [**OPM 設定 \_ \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)結構的 **abParameters** 成員包含 [**OPM \_ SET \_ HDCP \_ SRM \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)結構。
    -   [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)方法的 *pbAdditionalParameters* 參數會指向包含 SRM 的變數。
4.  傳送 [**OPM \_ 取得目前 \_ 的 \_ HDCP \_ SRM \_ 版本**](opm-get-current-hdcp-srm-version.md) 狀態要求至影片輸出。 使用傳送 [OPM 狀態要求](#sending-opm-status-requests)中所述的程式。 此狀態要求沒有輸入資料，因此 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構的 **abParameters** 成員內容未定義。
5.  當 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)方法傳回時， [**OPM 所 \_ 要求 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構中的 **abRequestedInformation** 陣列會包含 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構。 此結構的 **ulInformation** 成員包含目前 SRM 的版本號碼。 這個值必須等於步驟2中的值。

### <a name="enabling-hdcp"></a>啟用 HDCP

若要啟用 HDCP，請執行下列步驟。

1.  使用下列值，初始化 [**OPM \_ SET \_ 保護 \_ 層級的 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) 結構：
    -   **ulProtectionType**  = **OPM \_保護 \_ 類型 \_ HDCP**
    -   **ulProtectionLevel**  = **OPM \_HDCP \_**
    -   **保留** = 0
    -   **Reserved2** = 0
2.  傳送 [**OPM \_ SET \_ 保護 \_ 等級**](opm-set-protection-level.md) 命令。 **AbParameters** 陣列中的輸入資料是 [**OPM \_ SET \_ 保護 \_ 層級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)結構。
3.  傳送 [**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 等級**](opm-get-virtual-protection-level.md) 的狀態要求，以檢查是否已啟用 HDCP。 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構之 **abParameters** 成員的前4個位元組包含 **OPM \_ 保護 \_ 類型 \_** 的值。

當 [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)方法傳回時， [**OPM 所 \_ 要求 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構中的 **abRequestedInformation** 陣列會包含 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構。 此結構的 **ulInformation** 成員包含 [**OPM \_ HDCP \_ 保護 \_ 層級**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) 列舉中的值。 如果值等於 **OPM \_ HDCP \_**，即表示已啟用 hdcp。 否則，請重複步驟1至2，直到 HDCP 啟用，否則會發生錯誤。  (記得要遞增序號，並每次產生新的亂數字。 ) 

它通常需要100到200毫秒才能啟用 HDCP，但可能需要較長的時間。 除非您已確認，否則請不要將 HDCP 設定為已啟用。

當應用程式完成播放受保護的內容時，請關閉 HDCP。 這些步驟與啟用 HDCP 的步驟相同，但在步驟1中，將 **ulProtectionLevel** 設定 **為 \_ OPM \_ HDCP**。

> [!Note]  
> 如果連接器類型是 **OPM \_ 連接器 \_ 類型 \_ DISPLAYPORT \_ EMBEDDED**，請勿啟用 HDCP。  (參閱 [**OPM 連接器類型旗標**](opm-connector-type-flags.md)。 ) 

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 



