---
title: Windows 遠端管理詞彙
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106992245"
---
# <a name="windows-remote-management-glossary"></a>Windows 遠端管理詞彙


<dl> <dt>

wsman： Items * * * *
</dt> <dd>

在列舉中傳回的 WS-Management protocol 元素，可取得實例和實例 [*EPRs*](/windows)。 **wsman： Items** 是保存實例和其 EPR 的容器。 當要求中設定 **WSManFlagReturnObjectAndEPR** 旗標時，就會起始此類型的列舉。

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**基礎板管理控制器 (BMC)**
</dt> <dd>

在本機連接到伺服器的微控制器。 Bmc 的感應器會監視伺服器的實體狀態，以及可透過網路通訊的個別網路連線（即使伺服器已離線）。 您可以透過 [*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md) WMI 提供者來存取 BMC 資料。

</dd> <dt>

**基本驗證**
</dt> <dd>

驗證交換中傳送的使用者名稱和密碼。 基本驗證可以設定為在網域或工作組中使用 HTTP 或 HTTPS 傳輸。 這個方法是最不安全的驗證方法。

</dd> <dt>

**BMC**
</dt> <dd>

請參閱 [*(BMC)*](windows-remote-management-glossary.md)的基礎板管理控制器。

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Cim**
</dt> <dd>

請參閱 [*通用訊息模型 (CIM)*](windows-remote-management-glossary.md)。

</dd> <dt>

**客戶**
</dt> <dd>

使用 WS-Management 通訊協定的用戶端應用程式，以存取本機或遠端電腦上的管理服務。

</dd> <dt>

**通用訊息模型 (CIM)**
</dt> <dd>

[*分散式管理工作強制 (DMTF)*](windows-remote-management-glossary.md)模型，其描述如何代表真實世界的電腦和網路物件。 CIM 使用物件導向的開發架構，其中會使用類別和執行個體的概念來為 Managed 物件建立模型。

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**摘要式驗證**
</dt> <dd>

一種 exchange，其中伺服器會從用戶端接收要求，並將用戶端的相關資料傳送至驗證服務器，通常是網域控制站。 如果用戶端經過驗證，則伺服器會收到摘要工作階段金鑰，用來驗證用戶端的後續要求。

</dd> <dt>

**分散式管理工作強制 (DMTF)**
</dt> <dd>

業界組織開發企業和網際網路環境的管理標準與整合技術。

</dd> <dt>

**DMTF**
</dt> <dd>

請參閱 [*分散式管理工作強制 (DMTF)*](windows-remote-management-glossary.md)。

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**端點**
</dt> <dd>

[*端點參考可 (EPR)*](windows-remote-management-glossary.md)來定址的資源。

</dd> <dt>

**(EPR) 的端點參考**
</dt> <dd>

WS-Addressing 和 WS-Management 的組合，可同時描述 message SOAP 標頭中的資源位址。 這是 web 服務字詞。

</dd> <dt>

**列舉型別**
</dt> <dd>

[*資源*](windows-remote-management-glossary.md)實例的集合或集合，或要求這類集合的動作。 在 WS-Management 通訊協定中，會使用 [*WS-列舉*](windows-remote-management-glossary.md) 來取得集合。 在執行列舉的 WinRM 服務腳本時，會使用 [**Session. 列舉**](session-enumerate.md)[**和列舉值物件。**](enumerator.md) 對應的 c + + 方法和介面為 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) 和 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)。

</dd> <dt>

**EPR**
</dt> <dd>

請參閱 [*端點參考 (EPR)*](windows-remote-management-glossary.md)。

</dd> <dt>

**事件收集服務**
</dt> <dd>

從 BMC 和其他作業系統元件或應用程式接收事件的作業系統元件。

</dd> <dt>

**事件轉送**
</dt> <dd>

遠端電腦上發生的事件通知可以傳送至訂閱應用程式。 事件轉送不是 WinRM 的功能，而是 [Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔的功能。 在 Windows Vista 中，第一次可以使用事件轉送。 管理應用程式，例如 Microsoft Operations Manager (MOM) 使用事件轉送。

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

在要求中為 [*資源*](windows-remote-management-glossary.md)指定一組有限實例的查詢機制。 您可以對 [**Session**](session-enumerate.md)的呼叫指定 *篩選* 參數。列舉或 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。

</dd> <dt>

**篩選方言**
</dt> <dd>

XML 字串，識別用來在呼叫 [**Session. 列舉**](session-enumerate.md)或 [**Iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)中指定 [*篩選*](windows-remote-management-glossary.md)的 xml 方言。 WinRM 服務在接收要求時支援 [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) 作為篩選方言。

</dd> <dt>

**片段**
</dt> <dd>

XML 字串，可識別資源實例的一部分，而不是整個資源。 在 [**ResourceLocator**](resourcelocator.md) 物件中可找到片段支援。

</dd> <dt>

**片段方言**
</dt> <dd>

識別用來指定 [*片段*](windows-remote-management-glossary.md)之 xml 方言的 xml 字串。 在 [**ResourceLocator**](resourcelocator.md) 物件中可找到片段支援。 WinRM 服務在接收要求時支援片段方言的 [*XPath*](windows-remote-management-glossary.md) 。

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**頻內**
</dt> <dd>

用戶端應用程式會透過 [*作業系統中的*](windows-remote-management-glossary.md) WinRM 接聽程式取得 BMC 資料。

</dd> <dt>

**智慧型平臺管理介面 (IPMI)**
</dt> <dd>

適用于基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)的 IT 產業標準。 Windows 硬體管理功能提供了一種 [*IPMI 驅動程式*](windows-remote-management-glossary.md) 和 WMI [*IPMI 提供者*](windows-remote-management-glossary.md) ，可讓管理腳本、命令列工具和應用程式取得 BMC 資料。 IPMI 提供者具有 WMI [類別](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。

</dd> <dt>

**IPMI**
</dt> <dd>

請參閱 [*智慧型平臺管理介面 (IMPI)*](windows-remote-management-glossary.md)。

</dd> <dt>

**IPMI 驅動程式**
</dt> <dd>

核心驅動程式，可讓您從作業系統元件存取基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 裝置。

</dd> <dt>

**IPMI 提供者**
</dt> <dd>

標準的 WMI 提供者，定義將 [*IPMI*](windows-remote-management-glossary.md) 和其資料模型化的類別。 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)是從 BMC 取得資料的 COM DLL。

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

請參閱 [*鍵盤控制器樣式 (KCS)*](windows-remote-management-glossary.md)。

</dd> <dt>

**Kerberos 驗證**
</dt> <dd>

使用加密金鑰的用戶端和伺服器之間的相互驗證方法。 針對在 Windows 作業系統上執行的電腦，用戶端帳戶必須是與伺服器位於相同網域的網域帳戶。 當用戶端使用預設認證時，如果連接字串不是下列其中一項，則 Kerberos 是驗證方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。

</dd> <dt>

**鍵盤控制器樣式 (KCS)**
</dt> <dd>

[*IPMI 驅動程式*](windows-remote-management-glossary.md)用來與基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)通訊的通訊協定。

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

此管理服務會執行 WS-Management 通訊協定來傳送和接收訊息。 WinRM 是接聽程式服務。 接聽程式是由傳輸 (HTTP 或 HTTPS) 和 IPv4 或 IPv6 位址所定義。 您可以在單一電腦上建立一個以上的 WinRM 接聽程式實例，方法是為它們提供不同的 TCP/IP 位址或埠號碼。

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

在使用 [*SOAP*](windows-remote-management-glossary.md) 通訊協定所建立的電腦或個別網路之間傳輸的資訊套件。 封裝具有描述訊息目標和傳輸的標頭，以及包含訊息抵達時要使用之內容的主體。 訊息是來自規格的元素組合，例如 [*ws-addressing*](windows-remote-management-glossary.md)、 [*ws-Transfer*](windows-remote-management-glossary.md)和 [*ws-management*](windows-remote-management-glossary.md)。

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**命名 空間**
</dt> <dd>

[*Wmi*](windows-remote-management-glossary.md)命名空間，這是用來控制範圍和存取的 wmi 類別和實例的邏輯群組。 執行 Windows 之系統的管理資料最常見的來源是根 \\ cimv2 命名空間，其中包含 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)等類別。 例如，命名空間會出現在 WMI 類別的資源 URI 中 https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service 。

</dd> <dt>

**協商驗證**
</dt> <dd>

一種經過協商、單一登入的驗證類型，也就是 [*簡單且受保護的 GSSAPI 協商機制*](windows-remote-management-glossary.md)的 Windows 實作為 (SPNEGO) 。 SPNEGO 協商可判斷驗證是否由 Kerberos 或 NTLM 處理。 Kerberos 是慣用的機制。 以 Windows 為基礎的系統上的 Negotiate 驗證也稱為「Windows 整合式驗證」。

</dd> <dt>

**數值感應器**
</dt> <dd>

基礎板管理控制器中的感應器的數位類型 [*(BMC)*](windows-remote-management-glossary.md)，例如溫度或電壓。

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**選項**
</dt> <dd>

資源提供者處理要求所需的其他資料。 例如，某些 WMI 提供者需要提供其他資料做為 [**IWbemCoNtext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) 或 [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) 物件。 選項支援可在 [**ResourceLocator**](resourcelocator.md) 物件中找到。

</dd> <dt>

**頻外**
</dt> <dd>

用戶端應用程式會直接從另一部電腦的基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 取得資料，而不是透過作業系統中 [*的 WinRM 接聽*](windows-remote-management-glossary.md) 程式。

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**拉**
</dt> <dd>

系統會傳送 [*ws-列舉*](windows-remote-management-glossary.md) 提取訊息，以繼續初始呼叫 WS-列舉：列舉所啟動的列舉。 WinRM 服務中的提取作業是由列舉值 [**ReadItem**](enumerator-readitem.md) 或 [**IWSManEnumerator：： ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)所執行。

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**資源**
</dt> <dd>

代表不同類型之管理作業或值的 [*端點*](windows-remote-management-glossary.md) 。 服務會公開一或多個資源，而某些資源可以有一個以上的實例。 管理資源類似于 WMI 類別或資料庫資料表，而實例類似于類別的實例或資料表中的資料列。 例如， [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別代表資源。 `Win32_LogicalDisk="C:\"` 是資源的特定實例。

</dd> <dt>

**資源 URI**
</dt> <dd>

[*統一資源識別項 (URI)*](windows-remote-management-glossary.md)用來識別系統上特定類型的資源，例如磁片或處理常式。

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**基**
</dt> <dd>

請參閱 [*) 的系統事件記錄檔 (*](windows-remote-management-glossary.md)。

</dd> <dt>

**SEL 介面卡**
</dt> <dd>

將基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md) 資料傳送至 [*事件收集器*](windows-remote-management-glossary.md)的介面卡。

</dd> <dt>

**選取器**
</dt> <dd>

代表 [*資源*](windows-remote-management-glossary.md)之特定實例的名稱和值組。 這基本上是識別所需資源實例的篩選準則或「金鑰」。 在 [**ResourceLocator**](resourcelocator.md) 物件中找到選取器支援。

</dd> <dt>

**感應器**
</dt> <dd>

基礎板 [*管理控制器 (BMC)*](windows-remote-management-glossary.md)的測量裝置。

</dd> <dt>

**服務**
</dt> <dd>

透過 WS-Management 通訊協定和其他 [*web 服務*](windows-remote-management-glossary.md)提供管理服務給用戶端的應用程式。 服務通常會與 [*網路上的*](windows-remote-management-glossary.md) 接聽程式相同。 此服務具有實體傳輸位址。

</dd> <dt>

**會話**
</dt> <dd>

Windows 遠端管理 [*用戶端*](windows-remote-management-glossary.md) 與本機或 [*遠端 WinRM 接聽*](windows-remote-management-glossary.md)程式或服務之間的連接。 此連接類似于 WMI 用戶端腳本與遠端伺服器上的 WMI 之間的連接。 會話作業（例如列舉資源 (列舉) 、取得資源的實例 (取得) ，或執行資源方法 (叫用) 是 **會話** 物件的方法。 **Session** 物件是由 [**WSMan. CreateSession**](wsman-createsession.md)所建立。

</dd> <dt>

**簡單且受保護的 GSS-API 協商機制 (SPNEGO)**
</dt> <dd>

用戶端或伺服器在 Active Directory 內容中透過 WinRM 接收資料要求所使用的驗證機制。 SPNEGO 是以網際網路工程任務推動力 (IETF) 所產生的 (RFC) 通訊協定為基礎。 SPNEGO 也稱為「 [*Windows 整合式驗證*](windows-remote-management-glossary.md)」，這是 Windows 遠端管理說明主題中所使用的詞彙。

</dd> <dt>

**Simple Object Access Protocol (SOAP) - 簡易物件存取通訊協定 (Simple Object Access Protocol, SOAP)**
</dt> <dd>

Web 服務使用的 XML 架構通訊協定。

</dd> <dt>

**肥皂**
</dt> <dd>

請參閱 [*(SOAP) 的簡單物件存取通訊協定*](windows-remote-management-glossary.md)。

</dd> <dt>

**SPNEGO**
</dt> <dd>

查看 [*簡單且受保護的 GSS-API 協商機制 (SPNEGO)*](windows-remote-management-glossary.md)。

</dd> <dt>

**系統事件記錄檔 (的 SEL)**
</dt> <dd>

基礎板管理控制器中的事件資料庫 [*(BMC)*](windows-remote-management-glossary.md) 硬體。 「 [*SEL 介面卡*](windows-remote-management-glossary.md) 」會將這些事件傳達給作業系統。

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**(URI 的統一資源識別項)**
</dt> <dd>

識別企業中資源的字串，例如電腦、進程、磁片磁碟機或基礎板管理控制器中的溫度感應器 [*(BMC)*](windows-remote-management-glossary.md)。 URI 是在網際網路工程任務推動小組中定義的 web 服務定址機制 (IETF) 統一資源識別項 (URI) ：一般語法 \[ RFC3986 \] 。

</dd> <dt>

**URI**
</dt> <dd>

請參閱 [*(URI) 的統一資源識別項*](windows-remote-management-glossary.md)。

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**web 服務**
</dt> <dd>

軟體應用程式，用於跨網際網路或網路的電腦之間的互動。 Web 服務是由 [*Web 服務描述語言 (WSDL)*](windows-remote-management-glossary.md)所描述。 Web 服務的特定描述會告知其他服務如何使用 SOAP 訊息與 web 服務互動。 訊息是透過傳輸（通常是 HTTP 或 HTTPS）在電腦之間傳達。 [*Ws-addressing*](windows-remote-management-glossary.md)、 [*ws-事件*](windows-remote-management-glossary.md)和 [*ws-management*](windows-remote-management-glossary.md) 是 web 服務應用程式用來彼此通訊的通訊協定範例。

</dd> <dt>

**Web 服務描述語言 (WSDL)**
</dt> <dd>

用來定義如何與 web 服務互動的 XML 語言。 WSDL 通常會描述 web 服務在傳回資料或執行作業時所需要的 SOAP 訊息。 只要符合 WSDL 的需求，WSDL 就能讓某個作業系統的執行與另一個作業系統上所執行的 web 服務進行通訊。

</dd> <dt>

**Windows 整合式驗證**
</dt> <dd>

請參閱 [*協商驗證*](windows-remote-management-glossary.md)。

</dd> <dt>

**Windows Management Instrumentation (WMI)**
</dt> <dd>

Microsoft 對 Web-Based Enterprise Management (WBEM) 標準的實施是由 [*分散式管理工作強制 (的 DMTF)*](windows-remote-management-glossary.md)所發行。 WMI 可讓您使用 [*通用訊息模型 (CIM)*](windows-remote-management-glossary.md) 標準的延伸模組，來管理本機和遠端電腦，並將電腦和網路物件模型。

</dd> <dt>

**Windows 遠端管理 (WinRM)**
</dt> <dd>

Microsoft 會根據公用標準 [*ws-management*](windows-remote-management-glossary.md) 通訊協定來實行管理 web 服務。

</dd> <dt>

**Windows 遠端 Shell (WinRS)**
</dt> <dd>

依賴 [*Windows 遠端管理*](windows-remote-management-glossary.md) 執行遠端命令的 shell 工具，特別是針對無周邊伺服器。 命令列工具為 Winrs。

</dd> <dt>

**WMI**
</dt> <dd>

請參閱 [*(WMI) 的 Windows Management Instrumentation*](windows-remote-management-glossary.md)。

</dd> <dt>

**WMI 外掛程式**
</dt> <dd>

讓 WinRM 用戶端可以使用 WMI 資料的 WinRM 外掛程式。

</dd> <dt>

**WS-ADDRESSING (wsa)**
</dt> <dd>

公用標準通訊協定，它是以 SOAP 為基礎的通訊協定，它會建立在網際網路上傳送的訊息標頭中使用的定址系統。 標準定義如何跨網路和防火牆來找出資源。 WS-Addressing 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。

</dd> <dt>

**Wsen) 的 WS-列舉 (**
</dt> <dd>

公用標準通訊協定，它是以 SOAP 為基礎的，用來列舉 XML 元素序列，這些專案可能代表資料收集、記錄或其他線性資訊結構。 WS-Enumeration 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。

</dd> <dt>

**WS-事件 (wse)**
</dt> <dd>

公用標準通訊協定（以 SOAP 為基礎），可讓一個 web 服務 (訂閱者) 訂閱和接受來自另一個 web 服務 (事件來源) 的事件通知訊息。 WS-Eventing 是撰寫 WS-Management 通訊協定的其中一個 web 服務通訊協定。

</dd> <dt>

**WS-Management**
</dt> <dd>

公用標準通訊協定，它是以 SOAP 為基礎的通訊協定，可在所有作業系統、電腦和裝置之間共用管理資料。 WinRM 用戶端或伺服器元件所傳送的所有 [*訊息*](windows-remote-management-glossary.md) 都會使用此通訊協定。

</dd> <dt>

**WS-傳輸 (wxf)**
</dt> <dd>

公用標準通訊協定，它是以 SOAP 為基礎的，可透過一組簡單的動詞（例如 Get、Put、Invoke 或 Delete）來存取 web 服務型資源的 XML 標記法。 WS-Transfer 定義用於傳送和接收特定資源的標記法，以及用來建立或刪除資源及其對應表示的作業。

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

用來定址 XML 檔之部分的路徑標記法，類似于 URL。 XPath 運算式是要從 XML 檔中的目前位置取得至另一個節點或一組節點的片語序列。 片語會以正斜線分隔 ( "/" ) 個字元。 WinRM 服務支援 [*片段方言*](windows-remote-management-glossary.md)的 [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) 。

</dd> </dl>

 

 