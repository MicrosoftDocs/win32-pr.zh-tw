---
title: 使用 OLE DB 搜尋
description: 針對使用 ActiveX Data Objects (ADO) 和所有非自動化用戶端的 Automation 用戶端，ADSI 會提供支援 OLE DB 查詢介面子集的 OLE DB 提供者。
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- 使用 OLE DB ADSI 搜尋
- 查詢 ADSI，使用 OLE DB 搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683113"
---
# <a name="searching-with-ole-db"></a>使用 OLE DB 搜尋

針對使用 ActiveX Data Objects (ADO) 和所有非自動化用戶端的 Automation 用戶端，ADSI 會提供支援 OLE DB 查詢介面子集的 OLE DB 提供者。 已使用 OLE DB 介面進行查詢的用戶端程式代碼，可以使用相同的介面來查詢目錄服務。

在 OLE DB 的執行下，目錄服務會公開為數據源物件。 資料來源物件是會話物件的 factory，而且支援 [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) 以連接到目錄， [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) 建立會話物件， [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) 提供驗證資料給基礎命名空間，並提供查詢命令和 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) ，以將建立資料來源物件所需的資料儲存至基礎目錄服務。

**使用 OLE DB 執行 Active Directory 查詢**

1.  從 OLE DB 提供者取出 [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) 介面。 在 Active Directory 的情況下，請使用類別識別碼 **CLSID \_ ADsDSOObject**。
2.  建立連接資料的 [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) 陣列，並指定使用者名稱和密碼。
3.  查詢步驟1中針對[IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85))介面所取得的[IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85))介面。
4.  呼叫 [IDBProperties：： SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) 方法，在步驟2中建立的 [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) 陣列中傳遞。
5.  呼叫 [IDBInitialize：： Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) 方法，以建立與 OLE DB 提供者的連接;這是 Active Directory 提供者（在此情況下）。
6.  查詢[IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85))介面的[IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85))介面。
7.  呼叫 [IDBCreateSession：： CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) 方法，要求型別 [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85))的新介面。
8.  呼叫 [IDBCreateCommand：： CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) 方法來建立 [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) 介面。
9.  呼叫 [ICommandText：： SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) 方法。 傳入慣用的方言和該方言中的實際查詢命令文字。 可以使用 **Dbguid-sql \_ LDAPDialect** 或 **dbguid-sql \_ DBSQL** 做為方言。
10. 呼叫 [ICommand：： Execute](/previous-versions/windows/desktop/ms718095(v=vs.85));傳回 [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) 介面，這是結果集的介面。
11. 查詢[IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85))介面的[IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85))介面。
12. 呼叫 [IColumnsInfo：： GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) 方法，以取得有關結果集的資料行資料。
13. 填入 [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) 結構的陣列，描述 OLE DB 提供者如何將每個資料行的資料類型公開給應用程式程式碼。 此步驟可讓您指定要包含在特定資料行中的類型。 此外，資料行的位移（相對於傳回的資料列）在這裡是逐欄的設定。
14. 查詢[IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85))介面的[IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85))介面。
15. 呼叫 [IAccessor：： CreateAccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) 方法，這個方法會傳回存取子控制碼的陣列。 接著會使用這個陣列來存取結果集的資料列。
16. 呼叫 [IRowset：： GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) 傳入資料列控制碼，以及要取得的資料列數目。
17. 從步驟16傳回的集合中，呼叫 [IRowset：：](/previous-versions/windows/desktop/ms716988(v=vs.85)) 的資料列控制碼。 傳回資料列的原始指標。

如需搜尋篩選語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。

若要讀取所傳回未處理的資料列資料，請使用在步驟13中建立的 [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) 結構，計算步驟17所傳回之未處理資料指標中的資料行位移。 讀取資料行的狀態部分，以取得該資料行的抓取結果。

如需詳細資訊和示範如何使用 ADSI OLE DB 提供者來搜尋 Active Directory 的程式碼範例，請參閱 [使用 OLE DB 搜尋 Active Directory 的範例程式碼](example-code-for-using-ole-db-to-search-active-directory.md)。

 

 