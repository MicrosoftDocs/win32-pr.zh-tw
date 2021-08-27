---
description: 描述影片內容&\# 8211; 圖形驅動程式可提供的保護功能。
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based 內容保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e09829984273c35524fe9c8f3cd19e759e18dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465035"
---
# <a name="gpu-based-content-protection"></a>GPU-Based 內容保護

本主題說明圖形驅動程式可提供的影片內容-保護功能。

-   [簡介](#introduction)
-   [解碼流程的總覽](#overview-of-the-decoding-process)
-   [加密解碼的壓縮影片緩衝區](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. 查詢驅動程式的內容保護功能](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. 設定已驗證的通道](#2-configure-the-authenticated-channel)
    -   [3. 設定密碼編譯會話](#3-configure-the-cryptographic-session)
    -   [4. 取得 DXVA 解碼器裝置的控制碼](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. 將 DXVA 解碼器與密碼編譯會話產生關聯](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [傳送已驗證的通道命令](#sending-authenticated-channel-commands)
-   [傳送已驗證的通道查詢](#sending-authenticated-channel-queries)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

下圖顯示受保護的影片內容如何流經要轉譯之管線的簡化觀點。

![顯示受保護的影片內容的圖表。](images/d3d9video01.png)

> [!Note]  
> 此圖表不會描述 (PMP) 的 [受保護媒體路徑](protected-media-path.md) 。 此處所顯示的資料流程可能發生在 PMP 程式中，或在應用程式進程內。

 

此解碼器會從外部來源接收加密的壓縮影片資料。 此外，也會假設解碼器也會收到密碼編譯金鑰，以將此資料解密。 本主題不會說明影片來源與解碼器之間的金鑰交換，但 PMP 會定義一個可能的機制。 GPU 不包含在這個階段。

針對硬體加速解碼，軟體解碼器會將壓縮的影片內容傳遞給 GPU。 為了保護此內容，此解碼器會重新加密資料（通常是使用 AES CTR），再將它傳遞給硬體加速器。 金鑰交換器制是在解碼器和圖形驅動程式之間定義。

解碼的影片畫面會儲存在視訊記憶體中，通常是以純文字顯示。 此時，系統會處理框架並呈現出來。 簡報有兩個主要選項。

-   畫面格可以使用硬體重迭顯示。 如需詳細資訊，請參閱 [硬體覆蓋支援](hardware-overlay-support.md)。
-   桌面視窗可以顯示畫面格，以使用共用的表面來管理 (DWM) 。

最後一個步驟是在監視器上顯示畫面格，這可能需要在圖形配接器與顯示裝置之間進行連結保護。 High-Bandwidth 數位內容保護 (HDCP) ，就是連結保護的範例。 連結保護是使用 [輸出保護管理員](output-protection-manager.md) (OPM) 來設定。 本主題不會說明 OPM;如需詳細資訊，請參閱 [使用輸出保護管理員](using-output-protection-manager.md)。

## <a name="overview-of-the-decoding-process"></a>解碼流程的總覽

在硬體加速解碼期間，軟體解碼器必須將壓縮的影片資料傳遞到圖形配接器。 針對 premium 內容，此資料通常必須先使用對稱金鑰加密加密，才會傳送至 GPU。

若要加密影片進行解碼，軟體解碼器會使用下列介面：

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)。 代表 DXVA 解碼器裝置，也稱為快速鍵。
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)。 代表提供加密金鑰的密碼編譯會話。
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)。 代表已驗證的通道，可讓軟體解碼器將密碼編譯會話與 DXVA 解碼器產生關聯。

![顯示 direct3d9 解碼介面的圖表。](images/d3d9video02.png)

所有這些介面都是從 Direct3D 裝置取得，如下所示：



| 介面                                                                | 建立                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | 呼叫 [**IDirectXVideoDecoderService：： CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)。 DXVA 解碼器裝置是由 DXVA 設定檔 GUID 所識別。 |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | 呼叫 [**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)。                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | 呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)。                                                           |



 

> [!Note]  
> 若要取得 [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) 介面的指標，請在 D3D9Ex 裝置上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

 

經過驗證的通道會提供軟體解碼器與驅動程式之間的信任通道。 通道的運作方式如下：

-   驅動程式會提供其根憑證由 Microsoft 簽署的 x.509 憑證鏈。
-   憑證包含驅動程式的 RSA 公開金鑰。
-   軟體解碼器會使用公開金鑰來傳送128位 AES 工作階段金鑰給驅動程式。
-   軟體解碼器會將查詢和命令傳送給已驗證的通道。
-   工作階段金鑰是用來計算查詢和命令 (Mac) 的訊息驗證碼。 驅動程式會使用 Mac 來確認查詢/命令資料的完整性，而軟體解碼器會使用它們來確認驅動程式回應資料的完整性。

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>加密解碼的壓縮影片緩衝區

以下是加密和解碼流程的高階總覽：

1.  軟體解碼器會接收來自影片來源的加密資料串流。 此解碼會解密此資料流程。
2.  軟體解碼會使用密碼編譯會話來協商工作階段金鑰。
3.  軟體解碼器會使用已驗證的通道，將密碼編譯會話與 DXVA 解碼器裝置產生關聯。
4.  軟體解碼器會將壓縮的資料放在從 DXVA 解碼器裝置 (加速器) 取得的 DXVA 緩衝區中。 針對受保護的內容，軟體編碼器會使用工作階段金鑰進行加密，以將放置在 DXVA 緩衝區中的資料加密。
    > [!Note]  
    > 有些驅動程式會使用內容金鑰，而不是使用工作階段金鑰進行加密。 內容金鑰可從一個畫面格變更為下一個畫面格。

     

5.  此解碼器會將加密的壓縮緩衝區提交到加速器。 針對 AES CTR，此解碼器也會傳遞初始化向量。 如果使用內容金鑰，則此解碼會傳遞內容金鑰，並使用工作階段金鑰進行加密。

Direct3D 具有128位 AES CTR 的標準支援，但其設計目的是要延伸至其他加密類型。

接下來的五個章節會提供更詳細的步驟。

-   [1. 查詢驅動程式的內容保護功能](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. 設定已驗證的通道](#2-configure-the-authenticated-channel)
-   [3. 設定密碼編譯會話](#3-configure-the-cryptographic-session)
-   [4. 取得 DXVA 解碼器裝置的控制碼](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. 將 DXVA 解碼器與密碼編譯會話產生關聯](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. 查詢驅動程式的內容保護功能

嘗試套用加密之前，請先取得驅動程式的內容保護功能。

1.  取得 Direct3D 9 裝置的指標。
2.  呼叫 [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。
3.  呼叫 [**IDirect3DDevice9Video：： GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps)。 這個方法會在 [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) 結構中填入驅動程式的內容保護功能。

請特別注意下列功能：

-   如果 **Caps** 成員包含 **D3DCPCAPS_SOFTWARE** 或 **D3DCPCAPS_HARDWARE** 旗標，驅動程式就可以執行加密。
-   **KeyExchangeType** 成員會指定如何執行工作階段金鑰的金鑰交換。
-   如果 **Caps** 成員包含 **D3DCPCAPS_CONTENTKEY** 旗標，驅動程式會使用不同的內容金鑰進行加密。 當您產生工作階段金鑰時，這很重要。

**Caps** 成員中會指出額外的功能。

### <a name="2-configure-the-authenticated-channel"></a>2. 設定已驗證的通道

下一步是設定已驗證的通道。

1.  呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) 來建立已驗證的通道。 針對 *ChannelType* 參數，指定符合驅動程式功能的通道類型。
    -   **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** 通道類型對應到 **D3DCPCAPS_SOFTWARE**。
    -   **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** 通道類型對應到 **D3DCPCAPS_HARDWARE**。

    **CreateAuthenticatedChannel** 方法會傳回 [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)介面的指標，以及通道的控制碼。 稍後會使用此控制碼，將密碼編譯會話與已驗證的通道產生關聯。
2.  呼叫 [**IDirect3DAuthenticatedChannel9：： GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。 配置所需大小的緩衝區。
3.  呼叫 [**IDirect3DAuthenticatedChannel9：： GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) 以取得憑證。 方法會將憑證複製到在上一個步驟中配置的緩衝區。
4.  確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。
5.  從憑證取得公開金鑰。
6.  產生隨機的 RSA 工作階段金鑰。 此工作階段金鑰是用來簽署傳送至已驗證通道的資料。 使用驅動程式的公開金鑰來加密工作階段金鑰。
7.  呼叫 [**IDirect3DAuthenticatedChannel9：： NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。
8.  將安全通道初始化，如下所示：
    1.  填入檔中所述的 [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) 結構。
    2.  藉由呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)來傳送 [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md)命令，如傳送 [已驗證的通道命令](#sending-authenticated-channel-commands)一節中所述。 此命令包含傳送至已驗證通道之命令和查詢的起始序號。
9.  將 [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) 查詢傳送給已驗證的通道，以驗證通道類型，如傳送 [已驗證的通道查詢](#sending-authenticated-channel-queries)一節中所述。 檢查通道類型是否符合您在 [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) 方法中指定的專案。

### <a name="3-configure-the-cryptographic-session"></a>3. 設定密碼編譯會話

接下來，設定密碼編譯會話，並建立工作階段金鑰。

1.  呼叫 [**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) 來建立密碼編譯會話。 這個方法會傳回 [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) 介面的指標，以及密碼編譯會話的控制碼。
2.  呼叫 [**IDirect3DCryptoSession9：： GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。 配置所需大小的緩衝區。
3.  呼叫 [**IDirect3DCryptoSession9：： GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) 以取得憑證。 方法會將憑證複製到在上一個步驟中配置的緩衝區。
4.  確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。
5.  從憑證取得公開金鑰。
6.  產生隨機的 RSA 工作階段金鑰。 這是來自已驗證通道工作階段金鑰的個別工作階段金鑰。 使用驅動程式的公開金鑰來加密工作階段金鑰。
7.  呼叫 [**IDirect3DCryptoSession9：： NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。
8.  如果內容保護功能包含 **D3DCPCAPS_CONTENTKEY**，請建立隨機的 RSA 內容金鑰。 稍後會在解碼程式中使用這項功能。

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. 取得 DXVA 解碼器裝置的控制碼

在下一個步驟中，您將需要 DXVA 解碼器裝置的控制碼。 若要取得此控制碼，請填寫 DXVA2_DecodeExecuteParams 結構，如下所示：


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



將 [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams)結構的 **pExtensionData** 成員設定為 [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata)結構的位址。

在 [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) 結構中，將 **函數** 成員設定為 **DXVA2_DECODE_GET_DRIVER_HANDLE**。 將 **pPrivateOutputData** 設定為足以儲存 **控制碼** 值的緩衝區位址。  (在上述範例中，此緩衝區是 *hDecodeDeviceHandle* 變數。 ) 

然後呼叫 [**IDirectXVideoDecoder：： Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) 並傳入 [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) 結構的位址。 DXVA 解碼器的控制碼會在 **pPrivateOutputData** 中傳回。

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. 將 DXVA 解碼器與密碼編譯會話產生關聯

接下來，將 DXVA 解碼器裝置與 Direct3D 裝置和密碼編譯會話產生關聯，如下所示：

1.  取得 DXVA 解碼器裝置的控制碼，如上一節中所述。
2.  將 [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) 查詢傳送至已驗證的通道，以取得 Direct3D 裝置的控制碼。
3.  在 [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) 結構中填入下列資訊：
    -   將 **DXVA2DecodeHandle** 成員設定為 DXVA 解碼器裝置的控制碼。
    -   將 **CryptoSessionHandle** 成員設定為密碼編譯會話的控制碼。 [**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)方法會傳回這個控制碼。
    -   將 **DeviceHandle** 成員設定為 Direct3D 裝置控制碼。
4.  呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 以傳送 [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) 命令給已驗證的通道。

下圖說明控制碼的交換：

![此圖顯示 dxva 解碼器如何與密碼編譯會話相關聯。](images/d3d9video03.png)

軟體解碼器現在可以使用密碼編譯工作階段金鑰來加密壓縮的影片緩衝區。 每個壓縮的緩衝區都會有自己的初始化向量 (IV) 在 [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc)結構的 **pvPVPState** 成員中指定。

## <a name="sending-authenticated-channel-commands"></a>傳送已驗證的通道命令

定義了一組命令來設定已驗證的通道和設定各種內容保護。 如需命令清單，請參閱 [內容保護命令](content-protection-commands.md)。

若要將命令傳送至已驗證的通道，請執行下列步驟。

1.  填寫輸入資料結構。 此資料結構一律是 [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) 結構，後面接著其他欄位。 填寫 **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** 結構，如下表所示。

    
| member | 描述 | 
|--------|-------------|
| <strong>omac</strong> | 請立即略過此欄位。 | 
| <strong>ConfigureType</strong> | 識別命令的 GUID。 如需命令清單，請參閱 <a href="content-protection-commands.md">內容保護命令</a>。 | 
| <strong>hChannel</strong> | 已驗證通道的控制碼。 | 
| <strong>SequenceNumber</strong> | 序號。 第一個序號是藉由傳送 <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> 命令來指定。 每次您傳送另一個命令時，就會將此數位遞增1。 此序號會防止重新執行攻擊。    <blockquote>    [!Note]<br />    使用兩個不同的序號，一個用於命令，一個用於查詢。    </blockquote><br /><br /> | 


    

     

2.  針對出現在輸入結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。 然後將此標記值複製到 **omac** 成員中。
3.  呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。
4.  驅動程式會將命令的輸出放在 [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) 結構中。
5.  針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。 將此值與 **omac** 成員的值進行比較。 如果不相符，則會失敗。
6.  比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。 如果不相符，則會失敗。
7.  遞增下一個命令的序號。

## <a name="sending-authenticated-channel-queries"></a>傳送已驗證的通道查詢

系統會定義一組查詢來取得已驗證通道的相關資訊。 如需查詢清單，請參閱 [內容保護查詢](content-protection-queries.md)。

若要將命令傳送至已驗證的通道，請執行下列步驟。

1.  填寫輸入資料結構。 此資料結構一律是 [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) 結構，後面可能接著其他欄位。 填寫 **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** 結構，如下表所示。

    
| member | 描述 | 
|--------|-------------|
| <strong>QueryType</strong> | 識別查詢的 GUID。 如需查詢清單，請參閱 <a href="content-protection-queries.md">內容保護查詢</a>。 | 
| <strong>hChannel</strong> | 已驗證通道的控制碼。 | 
| <strong>SequenceNumber</strong> | 序號。 第一個序號是藉由傳送 <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> 命令來指定。 每次您傳送另一個查詢時，會將此數位遞增1。 此序號會防止重新執行攻擊。    <blockquote>    [!Note]<br />    使用兩個不同的序號，一個用於命令，一個用於查詢。    </blockquote><br /><br /> | 


    

     

2.  呼叫 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。
3.  驅動程式會將查詢的輸出放在 [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) 結構中。 根據查詢類型而定，這個結構後面會接著其他欄位。
4.  針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。 將此值與 **omac** 成員的值進行比較。 如果不相符，則會失敗。
5.  比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。 如果不相符，則會失敗。
6.  遞增下一個查詢的序號。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 9 影片 Api](direct3d-video-apis.md)
</dt> </dl>

 

 
