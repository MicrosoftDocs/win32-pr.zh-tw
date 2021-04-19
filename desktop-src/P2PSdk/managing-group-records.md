---
description: 群組記錄是發佈至對等群組的所有作用中成員的特定資料，例如聊天訊息或應用程式特定的狀態更新。
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: 管理群組記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d9e3257cc597b715dc9c65eb5945c00c15286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987540"
---
# <a name="managing-group-records"></a>管理群組記錄

群組記錄是發佈至對等群組的所有作用中成員的特定資料，例如聊天訊息或應用程式特定的狀態更新。 記錄是以 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構表示，並包含下列有關對等的資訊：

-   記錄識別碼是可唯一識別對等群組中之記錄的值。
-   指定記錄類型的 GUID。 應用程式可支援不同的記錄類型。 應用程式會根據記錄類型來解讀記錄的 **資料** 欄位。 某些 Guid 是保留的，而且 API 呼叫會在應用程式嘗試使用時，傳回 **\_ \_ 未 \_ 授權的對等 E** 。
-   描述為 XML 字串的一組記錄屬性。 搜尋記錄時，會使用屬性。 如需屬性的詳細資訊，請參閱 [記錄屬性架構](record-attribute-schema.md)。
-   建立記錄的對等時間。
-   記錄到期的對等時間。
-   修改記錄的對等時間。
-   記錄的建立者。
-   修改記錄的成員。
-   [**對等 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_data)結構，包含此 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)結構中所有欄位的密碼編譯簽章。 對等不能直接更新或修改此欄位。
-   [**對等 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_data)結構，其中包含與此記錄相關聯的應用程式特定資料，做為位元組陣列。 這個欄位中的資料類型是由應用程式定義的記錄類型所決定。

## <a name="obtaining-peer-group-records"></a>取得對等群組記錄

藉由呼叫 [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) 與記錄的識別碼，即可取得個別記錄。 處理特定類型的所有記錄時，會先呼叫 [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) 來開啟列舉，然後反復呼叫 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) ，直到所有記錄都被抓取，藉以取得所有目前對等群組記錄的列舉集合。 完成時，請藉由呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)來關閉列舉並釋放與其相關聯的記憶體。

當對等體建立、刪除或更新記錄時，受影響的記錄會透過 **對等 \_ 群組 \_ 事件 \_ 記錄 \_ 變更** 事件發行至對等群組的所有成員。 請注意，如果對等互連未連接到群組，它會在下次連線時接收更新的記錄。 如果您的應用程式以任何有意義的方式維護或記錄管理，請務必使用 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) 註冊此事件。 或者，應用程式可以使用 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)視需要查詢記錄資料庫。

當 **對等 \_ 群組 \_ 事件 \_ 記錄 \_ 變更** 事件引發時，將會收到特定的記錄識別碼和類型，以及變更的類型 (新增、更新、刪除) 會被視為 [**對等 \_ 事件 \_ 記錄 \_ 變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) 結構。 此結構是透過呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)來取得。 如果變更是新增或更新，您應該使用 [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) 取得具有所提供識別碼的記錄。 基礎結構的本機記錄資料庫會自動更新。

您也可以根據 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)的 **pwzAttributes** 欄位中提供的特定自訂屬性以及任何預先定義的屬性，來搜尋特定的記錄。 若要完成此動作，請使用 [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) 函式搭配 [ [記錄搜尋查詢格式](record-search-query-format.md) ] 主題中指定的 XML 搜尋查詢格式。

如需使用對等基礎結構中記錄的詳細資訊，請參閱[使用對等基礎結構](using-the-peer-infrastructure.md)中的[記錄](records.md)主題。

## <a name="administration-of-peer-group-records"></a>對等群組記錄的管理

當對等群組的建立者發出初始邀請時，它可以指定特定成員在系統管理角色中提供 (對等 \_ 群組 \_ 角色系統 \_ 管理員) 只要透過 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) 或 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)) 向使用者 (發出新認證。 系統管理員可以直接新增、刪除及更新任何對等群組記錄。 相反地，如果對等群組成員的角色設定為 **對等 \_ 群組 \_ 角色 \_ 成員** 或 **對等群組角色，則 \_ \_ \_ 邀請 \_ 成員** 的對等群組成員只能新增、更新及刪除其本身的記錄 (s) 。

建立者預設具有系統管理員角色。

若要更新記錄，請取得具有 [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) 或 [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)的記錄、進行變更，然後將更新的記錄傳遞至 [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)。

若要刪除記錄，請將記錄識別碼傳遞至 [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)。

若要新增記錄，請建立新的 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構，並填入下欄欄位：

-   **dwSize**。 此欄位包含 **sizeof** ([**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)) 的值。
-   **ftExpiration**。 此欄位包含此記錄的到期日期和時間，以對等時程表示為 **FILETIME** 結構。
-   **輸入**。 此欄位包含識別應用程式之記錄類型的 **GUID** 值。 如果此類型是您應用程式基礎結構的自訂，您也應該填入 **資料** 欄位。

下欄欄位會由基礎結構填入，且如果應用程式設定，則會予以忽略：

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

其餘欄位是選擇性的。 若要將這個新記錄加入至對等群組，請將它傳遞給 [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)。

## <a name="importing-and-exporting-records"></a>匯入和匯出記錄

對等群組記錄會以資料庫的形式在本機進行維護。 若要將對等群組記錄資料庫的目前快照集儲存到本機檔案，請呼叫 [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)，並將控制碼傳遞給對等群組。 然後，您可以將此檔案傳輸到不同的電腦或應用程式，藉由呼叫 [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)來解壓縮和使用此記錄資料庫。

 

 



