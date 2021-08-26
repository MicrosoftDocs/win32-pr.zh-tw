---
title: 使用 Windows 部署服務伺服器 API
description: 在無法使用標準 Windows 部署服務 (WDS) 解決方案的環境中，wds 伺服器會公開可讓開發人員撰寫外掛程式（稱為提供者）的 API，以處理 (PXE) 要求的啟動載入器執行環境。
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows使用伺服器 API Windows 部署服務部署服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ce7516e5279fecdfeecfa90edd8e3a0dad265562fa5ea59336367dbe157c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999568"
---
# <a name="using-the-windows-deployment-services-server-api"></a>使用 Windows 部署服務伺服器 API

在無法使用標準 Windows 部署服務 (WDS) 解決方案的環境中，wds 伺服器會公開可讓開發人員撰寫外掛程式（稱為提供者）的 API，以處理 (PXE) 要求的啟動載入器執行環境。 撰寫適用于 WDS 的 PXE 提供者時，開發人員應該遵循下列指導方針。

## <a name="install-the-wds-role-on-the-server"></a>在伺服器上安裝 WDS 角色

-   Windows部署服務 (WDS) 是 (RIS) 的遠端安裝服務修訂版本，您將需要 WDS 伺服器角色才能執行 WDS PXE 伺服器和提供者。
-   WDS 將 RIS 取代為從 Windows Server 2008 開始的標準元件，以及 Windows server 2003 Service Pack 2 (SP2) 。
-   您必須將 RIS 伺服器更新為 Windows server 2003 Service Pack 1 (SP1) 上的 WDS。 您可以使用[Windows 自動安裝套件 (WAIK) ](https://www.microsoft.com/download/details.aspx?id=10333)來安裝 WDS 伺服器角色。

## <a name="register-providers"></a>註冊提供者

-   在安裝期間，將提供者動態連結程式庫 (DLL) 註冊，然後將提供者插入已註冊之提供者的已排序清單中。
    > [!Note]  
    > 當您安裝新的或修改的提供者時，您必須重新開機 WDS PXE 服務，變更才會生效。

     

-   使用 [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) 函式來註冊提供者，並將其新增至清單。 使用 [**PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) 函式取消註冊已註冊的提供者，並將它從清單中移除。
-   在排序的清單中指定提供者的順序。 無法保證清單中的提供者索引，因為稍後可能會先註冊另一個提供者。 若要將提供者插入到另一個已註冊的提供者之前或之後的清單中，請先使用 [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) 函式取得已註冊之提供者的索引，然後在指定較大或較小的索引值時註冊新的提供者。
-   安裝程式可以將提供者設定資訊儲存在註冊提供者時所傳回的登錄機碼下。 登錄機碼的位址是由 [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister)的 *phProviderKey* 所接收。 提供者會收到此相同索引鍵的控制碼，作為其 [*PxeProviderInitialize*](pxeproviderinitialize.md)回呼的 *hProviderKey* 參數。 提供者應儲存此金鑰的位址。
-   一律將提供者動態連結程式庫 (DLL) 安裝在伺服器的 [Program Files] 資料夾中。

## <a name="initialize"></a>初始化

-   包含在提供者中匯出 [*PxeProviderInitialize*](pxeproviderinitialize.md) 回呼函式的 DLL。 每個提供者都需要 *PxeProviderInitialize* 回呼。 當 WDS 載入提供者時，它會呼叫提供者的 *PxeProviderInitialize* 函式，並將控制碼傳遞至在提供者註冊期間用來儲存設定資訊的相同金鑰。
-   當 [*PxeProviderInitialize*](pxeproviderinitialize.md) 回呼傳回且成功時，提供者應該完全初始化並準備好處理要求。
-   在處理 [*PxeProviderInitialize*](pxeproviderinitialize.md) 函式期間，在提供者中註冊每個回呼。 回呼應該向 [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函式註冊。
-   在處理其 [*PxeProviderInitialize*](pxeproviderinitialize.md) 函式時，初始化所有提供者的內部資源。

## <a name="shutdown"></a>關機

-   執行 [*PxeProviderShutdown*](pxeprovidershutdown.md) 回呼。 每個提供者都必須有 *PxeProviderShutdown* 回呼。
-   [*PxeProviderShutdown*](pxeprovidershutdown.md)回呼函式應完全關閉提供者，並釋放其所有資源。
-   在 [*PxeProviderShutdown*](pxeprovidershutdown.md)回呼傳回之後，傳遞給 [*PxeProviderInitialize*](pxeproviderinitialize.md)函式的 *hProvider* 控制碼將不再有效，且不應該用來呼叫 WDS。
-   在處理 [*PxeProviderInitialize*](pxeproviderinitialize.md)回呼期間，透過 **PXE \_ 回呼 \_ 關機** 來呼叫 [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback)函式，以註冊 [*PxeProviderShutdown*](pxeprovidershutdown.md)回呼。 如果 *PxeProviderInitialize* 函數失敗，請勿呼叫 *PxeProviderShutdown* 回呼。

## <a name="handle-request-packet"></a>處理要求封包

為提供者執行 [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) 回呼。 每個提供者都必須有 *PxeProviderRecvRequest* 回呼。 當 WDS 收到要求時，它會呼叫已註冊之提供者清單中第一個提供者的 *PxeProviderRecvRequest* 回呼。

-   如果提供者會以同步方式處理此要求， [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) 函數應該會傳回「 **錯誤 \_ 成功**」的值。 只有在提供者將以非同步方式處理此要求時， *PxeProviderRecvRequest* 回呼應該會傳回 **錯誤 \_ IO \_ 暫** 止，並在處理要求時呼叫 [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) 函數。
-   [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)回呼和 [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)函式會傳回 **PXE \_ 開機 \_ 動作** 列舉的位址，以描述提供者處理要求所採取的動作。

    提供者有四種方式可處理要求：

    -   提供者會使用包含網路開機程式路徑的標準 DHCP 回應封包來回複用戶端。 傳回列舉的 **PXE \_ BA \_ NBP** 值表示提供者已成功處理要求封包，並藉由呼叫 [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) 和 [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) 函式來傳送回應封包來完成要求。
    -   提供者會使用不符合 DHCP 的自訂回應封包來回複用戶端。 傳回列舉的 **PXE \_ BA \_ 自訂** 值表示提供者已成功處理要求封包，並藉由呼叫 [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) 和 [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) 函式來傳送自訂回應封包來完成要求。
    -   提供者會決定應忽略的要求。 傳回 **PXE 的 \_ [ \_ 略** 過列舉值] 表示提供者已釋放與要求相關聯的所有資源，且要求未傳遞給已註冊之提供者清單中的下一個提供者。 如果提供者偵測到要求封包無效，則可以使用此選項。
    -   提供者會拒絕為要求提供服務。 傳回列舉的 **PXE \_ BA \_ 拒絕** 值，會指示系統將要求傳遞給已註冊之提供者清單中的下一個提供者。 如果這是清單中的最後一個提供者，則會釋放與要求相關聯的所有資源，並忽略要求。
    -   在處理 [*PxeProviderInitialize*](pxeproviderinitialize.md)回呼期間，透過 **PXE \_ 回呼 \_ 接收 \_ 要求** 來呼叫 [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback)函式，以註冊 [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)回呼。

## <a name="generate-response-packet"></a>產生回應封包

-   使用 API 來寫入提供者來處理 DHCP 要求並產生回應封包。
-   [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)函數會指定提供者用來篩選封包的屬性。 您可以指定提供者的屬性，讓提供者查看所有封包，提供者只會看到 DHCP 封包，或提供者只看到指定 DHCP 廠商類別識別碼選項的 DHCP 封包 (60) 為 "PXEClient"。
-   [**PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)函數會檢查封包是否為有效的 DHCP 封包。 當使用 [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)函式設定的篩選器設定為接收所有封包，以判斷指定的封包是否為有效的 dhcp 封包時，提供者可以使用 **PxeDhcpIsValid** 函數來檢查來自用戶端的封包是否為 DHCP 封包。
-   [**PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)函式會根據從用戶端收到的封包中的資訊，將回應封包初始化為 DHCP 回復封包。 [*PxeProviderInitialize*](pxeproviderinitialize.md)函式會接受從 [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)回呼中的用戶端接收之有效 DHCP 封包的位址。 **PxeDhcpInitialize** 函式會採用以 [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate)函式所配置的回復封包指標。
-   [**PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)函式會從 DHCP 封包捕獲選項值。 [**PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue)函式會從 DHCP 封包 (43) 中，抓取廠商專屬資訊欄位的選項值。
-   然後，提供者可以使用資訊來填入回復封包，並使用 [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) 函式將回復封包傳送給用戶端。 [**PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)函數會將 DHCP 選項附加至回復封包。
-   藉由傳送封包來回複用戶端要求的提供者，必須使用 [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) 函數來配置回應封包。 然後，提供者可以使用資訊來填入回復封包，並使用 [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) 函式將回復封包傳送給用戶端。
-   當不再需要配置的記憶體時，提供者應該使用 [**PxePacketFree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) 函式來釋放它。

## <a name="enumerate-registered-providers"></a>列舉已註冊的提供者

-   使用 API 來撰寫提供者，以列舉和檢查清單中其他已註冊的提供者。
-   [**PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo)函數會傳回 PXE 伺服器的相關資訊。 **PxeGetServerInfo** 函式會傳回 **布林** 值，指出是否已啟用伺服器的追蹤。 **TRUE** 表示已啟用追蹤。
-   [**PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)函式會在已註冊的提供者清單中啟動 enumerationof 提供者。 **PxeProviderEnumFirst** 函式會啟動列舉，並傳回呼叫 [**PxeProviderEnumNext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)函數時應使用的控制碼位址。 **PxeProviderEnumNext** 函式會傳回 [**PXE \_ 提供**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)者結構，其中包含提供者的相關資訊。 [**PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)函式會釋放由 **PxeProviderEnumNext** 函數配置給 **PXE \_ 提供者** 結構的記憶體。 [**PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)函式會關閉已註冊之提供者清單中的提供者列舉。

## <a name="handle-service-control-codes"></a>處理服務控制碼

-   當收到服務控制訊息時，WDS 會呼叫 [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) 回呼。
-   提供者可以定義 [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) 回呼函式來處理服務控制訊息。
-   在處理 [*PxeProviderInitialize*](pxeproviderinitialize.md)回呼期間，透過 **PXE \_ 回呼 \_ 服務 \_ 控制** 呼叫 [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback)函式，以註冊 [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)回呼。

## <a name="add-trace-entries-to-pxe-log"></a>將追蹤專案新增至 PXE 記錄檔

-   [**PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace)函式會將追蹤專案加入至 PXE 記錄檔。 WDSPXE 會提供追蹤來協助系統管理員進行疑難排解。 提供者可以記錄不同嚴重性層級的追蹤專案。 系統管理員可以將 WDSPXE 設定為只記錄特定嚴重性層級的專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 部署服務 API](about-the-windows-deployment-services-api.md)
</dt> <dt>

[使用 Windows 部署服務用戶端 API](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




