---
description: 下列程式描述如何使用 ATL 版本2.1 或 ATL 3.0 版和 MSP 基類來執行 MSP。
ms.assetid: 7485c34a-3c8a-412f-9cb9-8eb895084292
title: 使用 TAPI 3 MSP 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ad4fd160cf0fc4c7dd682a44f3a4ff0bcec25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978163"
---
# <a name="using-the-tapi-3-msp-base-classes"></a>使用 TAPI 3 MSP 基類

下列程式描述如何使用 ATL 版本2.1 或 ATL 3.0 版和 MSP 基類來執行 MSP。 如需詳細資訊以及程式庫和標頭的清單，請參閱 [TAPI 3 MSP 基類](tapi-3-msp-base-classes.md)。 本主題中所包含的內容假設開發人員對 ATL 和 COM 有良好的瞭解，而且具有使用 ATL 來執行 COM Dll 的體驗。

**使用 ATL 2.1 或 ATL 3.0 執行和 MSP**

1.  為您的 MSP 建立 IDL 檔案。 此檔案會定義您 MSP 的 CLSID。 將您的 MSP "coclass" 宣告為執行 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) 介面，並將此介面宣告為類別物件上的預設介面。 針對 **ITMSPAddress** 的定義，匯入 ".msp" 檔案。 在您的 MSP 型別程式庫中包含 MSP "coclass"。 如果您的 MSP 支援私用 (自訂) 介面，請在這裡定義它們，並將它們包含在您的類型程式庫中。 下列程式碼範例是前述的 IDL 檔案，沒有自訂介面。

    ``` syntax
    import "msp.idl";
    [
          uuid(4DDB6D35-3BC1-11d2-86F2-006008B0E5D2),
          version(2.0),
          helpstring("Wave MSP 2.0 Type Library")
    ]
    library WAVEMSPLib
    {
    importlib("stdole32.tlb");
    importlib("stdole2.tlb");

    [
    uuid(4DDB6D36-3BC1-11d2-86F2-006008B0E5D2),
    helpstring("Wave MSP Class")
    ]
    coclass WaveMSP
    {
    [default] interface ITMSPAddress;
    };
    };
    ```

2.  當 Tapi3.dll 要求您的 TSP 時，請修改您的 TSP 以通告 MSP 的 CLSID。 確定 (1) 您的 TSP 可以 \_ \_ 在 TSPI 函式 [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)、 (2) 您的 tsp [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) 結構在 \_ **LINEDEVCAPFLAGS** 成員中設定 dwDevCapFlags msp 旗標，並 (3) 您的 tsp 在 TSPI 函式 [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)中傳回您的 msp CLSID。 這應該是您 IDL 檔案中指定的相同 CLSID;例如，在上一個步驟中，範例 IDL 檔案的第二個 "uuid" 行。
3.  編譯位於平臺軟體發展工具組 (SDK) 中的 MSPBase 範例應用程式，以建立 MSPBaseSample .lib 程式庫。
4.  將您的 MSP DLL 連結至 MSPBaseSample .lib 程式庫。
5.  從適用于 MSP 基礎類別定義的 SDK 包含 Mspbase。
6.  執行您的 DLL 匯出 (例如 DllMain) 。 Microsoft Visual C++ 會為您產生這些。 在 DllMain 中，分別在 DLL \_ 進程 \_ 附加和 dll 進程卸離上， \_ \_ 使用 **MSPLOGREGISTER** 和 **MSPLOGDEREGISTER** 宏來啟用 DLL 的記錄功能。 在 **MSPLOGDEREGISTER** 呼叫中指定您的 DLL 名稱。
7.  使用 Msplog 中定義的記錄宏，以與基類相同的方式輸出追蹤訊息。 定義 MSPLOG 預處理器符號，以在您的 DLL 中包含記錄;保持未定義狀態，以建立沒有記錄的 DLL。
8.  從可針對您的 MSP 執行位址的 CMSPAddress 衍生類別。 宣告全域 ATL 物件對應，當系統要求您在 IDL 檔案中指定的 CLSID 上 **CoCreate** 時，它會指示 ATL 建立您的網址類別別的實例。 此外，從 ATL **CComCoClass** 範本衍生您的 address 類別，並 \_ \_ 在您的 ADDRESS 類別中包含 DECLARE REGISTRY RESOURCEID 宣告。 針對任何其他 ATL COM DLL，建立對應的資源腳本和標頭檔。
9.  為您的 address 類別執行必要的 CMSPAddress 覆寫。 針對 [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref) 和 [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease)，請呼叫提供的 helper 函式範本。 針對 [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes)，只需將所有支援 MSP 的 TAPIMEDIAMODEs Or 運算傳回 **DWORD** 點陣圖。 若為 [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall) 和 [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)，請傳回 E \_ >notimpl，並在此時編譯並連結您的 MSP。 現在，請確認您可以從 TAPI 3 應用程式註冊並具現化您的 MSP，但無法成功建立呼叫。
10. 從 CMSPCallMultiGraph 衍生類別，以執行您的 MSP 呼叫物件。 如果每個資料流程的篩選-graph 模型不符合您的需求，您可能會想要從 [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase) 衍生而不是 [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph) ：這會增加工作 (的複雜度，在撰寫本文的同時，所有 Msp 都會直接從 **CMSPCallMultiGraph**) 衍生呼叫物件。 在您的 address 物件中，使用所提供的 helper 函式範本，執行 [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall) 和 [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall) 來建立和關閉特定類型的呼叫物件。 在您的呼叫物件中，覆寫 [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject) 以傳回 E \_ >notimpl。 以與對應的位址方法相同的方式覆寫 [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref) 和 [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease) 。 同樣地，您應該能夠編譯及連結您的 MSP;它現在應該可以建立和關閉呼叫，但是呼叫不會進行任何有用的串流。
11. 從 CMSPStream 衍生類別，以執行您的 MSP 資料流程物件。 在您的呼叫物件中，執行 [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)來建立和初始化您的資料流程物件 (通常是藉由呼叫 atl **CreateInstance** ，接著呼叫 atl **\_ InternalQueryInterface** for [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) ，然後在資料流程物件) 上呼叫 **Init** 。 若要支援固定數量的資料流程 (這通常適用于 Msp，不支援由呼叫) 上的其他端點修改串流設定，請覆寫呼叫物件上的 **Init**、 [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream)和 [**RemoveStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-removestream) 。  (呼叫 **Init** 一開始會建立所有的串流， **CreateStream** 和 **REMOVESTREAM** 會傳回適當的 TAPI 錯誤碼，以防止應用程式建立或移除資料流程) 。 否則，請覆寫呼叫的 **Init** 方法，以使用要求呼叫的媒體類型來建立資料流程的初始預設設定。 當您在呼叫的 **Init** 方法中建立任何預設資料流程物件時，請使用 [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) helper 方法。
12. 執行您的資料流程物件。 唯一需要的覆寫是 [**get \_ name**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-get_name) 方法，它只會傳回資料流程的易記名稱。 此外，您還需要覆寫其他數個方法。 確切要覆寫的方法取決於您的執行方式，以及當您決定要執行用來建立和解構篩選圖形時所涉及的各種工作。 這些工作包括建立適當的「傳輸」篩選器、編解碼器等，並在適當的時間從篩選圖形中插入和移除它們。 您也必須在終端機物件上使用 [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) 介面，將選取的終端機連接到您的串流。 您可能會想要覆寫資料流程物件上的 [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) 和 [**UnselectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-unselectterminal) ，以限制串流將接受的終端機設定;將每個資料流程限制為單一終端機，特別簡化了篩選圖形的結構，但會犧牲影片預覽等應用程式功能。 根據您的執行方式，您會將圖形結構、解構和終端機連接程式碼放在 [**StartStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-startstream)、 [**StopStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-stopstream)、 [**PauseStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-pausestream)、 [**Initialize**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)、 [**Shutdown**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)、 [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)和 [**UnselectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-unselectterminal) 方法中，或根據私用 TSP 通訊以您自己的方法來放置。 請注意，未選取終端機的資料流程必須追蹤所需的圖表狀態;在這類資料流程上，後面接著 **SelectTerminal** 呼叫的 **StartStream** 呼叫必須產生資料流程。 覆寫這些方法的大部分，以確保每個案例中都有正確的結構、解構、連接和中斷連接，視資料流程的狀態而定。
13. 實行您的 TSP 通訊。 覆寫 [**CMSPAddress：： ReceiveTSPAddressData**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata) 和/或 [**CMSPCallBase：： ReceiveTSPCallData**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-receivetspcalldata)，以及/或藉由呼叫您的 Address 物件上的 [**PostEvent**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-postevent) ，或從) 呼叫或資料流程物件 (呼叫物件上的 [**HandleStreamEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-handlestreamevent) 來覆寫。
14. 在您的 address 物件上使用 PostEvent，或在您的呼叫物件上使用從呼叫或串流物件 () ，以透過 Tapi3.dll 將呼叫媒體事件傳送至應用程式。 您通常會在資料流程物件上執行這項作業，方法是在覆寫的方法中，包括 [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent)、 [**StopStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-stopstream)、 [**StartStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-startstream)、 [**PauseStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-pausestream)、 [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)和 [**UnselectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-unselectterminal) 方法（視您的串流執行方式而定）。
15. 在您現有的物件上執行任何所需的私用介面或子串流， (address、call 和 stream) 。 通常不會有任何內容。 請注意，在執行私用介面時，請從 IDL 檔案指定類型程式庫的 LIBID。 也就是說，當您使用自訂介面時，應用程式設計人員必須使用您的 MSP 類型程式庫。 在 MSP 基類中執行的標準 MSP 介面會使用 Tapi3.dll LIBID，因此可供所有 TAPI 3 應用程式存取。
16. 如果針對預設靜態終端機執行 MSP 專屬靜態或動態終端機物件或取代 (不是一般) ，您可以使用提供的終端基類。 您必須覆寫位址物件上的各種方法，以提供建立終端機物件的替代方法或其他方法。
17. 在您的位址、呼叫、串流和終端機物件上，執行 IObjectSafety 介面。 若要使用 [分派](dispatch-mapper.md) 對應程式來查詢 MSP 物件上的介面，請將您的物件標示為安全，以在這些介面上編寫腳本。 若要這樣做，請在您的物件上執行 **IObjectSafety** 介面。 衍生自 **CMSPObjectSafetyImpl** () Msputils 中提供的 helper 類別，並將 **IObjectSafety** 新增至您類別的 ATL COM \_ 對應，可讓您的物件安全地在其公開的所有介面上編寫腳本。 請注意，在 MSP 物件上使用分派對應程式可能是隱含的。 MSP 位址和 MSP 呼叫是由 TAPI 位址和 TAPI 呼叫物件來匯總。 如果在 TAPI 物件上使用分派對應程式來查詢匯總的 MSP 物件所公開的介面，將會查詢匯總的 MSP 物件以取得所要求介面的安全。

 

 
