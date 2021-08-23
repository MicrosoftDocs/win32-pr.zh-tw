---
description: 您可以使用 identity Manager 和群組 Api 中的身分識別匯入和匯出函式，將對等身分識別和群組設定檔案匯入和匯出至另一個端點。
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: 身分識別和群組設定匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0102bda821b7157edc512aeea4a8e315c0dbfa1def85f9a61919ec0f2c86da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519328"
---
# <a name="identity-and-group-configuration-import-and-export"></a>身分識別和群組設定匯入和匯出

您可以使用 identity Manager 和群組 Api 中的身分識別匯入和匯出函式，將對等身分識別和群組設定檔案匯入和匯出至另一個端點。 這些功能很有用，因為它們可讓使用者快速且方便地將身分識別和群組設定資訊從一部電腦匯出到另一部電腦。

## <a name="importing-and-exporting-peer-identity-data"></a>匯入和匯出對等身分識別資料

藉由呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) 以及要匯出的身分識別名稱，以及用來加密相關聯認證的密碼，匯出對等的身分識別資料。 此函式會傳回 XML 字串，其中包含對等的身分識別名稱，以及該特定身分識別的加密認證，然後使用外部傳輸機制（例如電子郵件）將其傳遞至不同的電腦。 下列範例會顯示 XML 字串的格式：

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

您可以藉由呼叫 [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)來抓取匯出的身分識別資料，並以前一次呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)中提供的密碼傳入 XML 字串。 此函式會傳回匯入之身分識別的對等名稱。 匯入的身分識別名稱和認證可以像 [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) 或 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)所傳回的身分識別名稱一樣使用。

> [!Note]  
> 呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)時，應用程式或 API 使用者必須提供具有足夠長度的強式密碼。 這點很重要，因為匯入的身分識別資料包含身分識別的私密金鑰。

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>匯入和匯出群組身分識別設定

對等群組可讓對等使用特定的匯入和匯出 Api，將群組設定資料從某個端點匯出至另一個端點。 若要匯入設定資料，執行匯入 (之對等的身分識別，以及先前執行匯出) 的電腦必須存在於要匯入設定資料的電腦上。 您可以藉由使用本主題上一節中指定的方法來匯出和匯入此身分識別：匯 [入和匯出對等身分識別資料](#importing-and-exporting-peer-identity-data)。

群組設定資料包含身分識別的所有資訊，以從新的端點加入群組。 具體而言，設定資料包含 GMC 鏈、群組對等名稱、雲端名稱、範圍，以及一組 PNRP 特定旗標。 若為擁有群組的身分識別，群組設定資訊中就會包含該群組的私密金鑰。

> [!Note]  
> 呼叫 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)時，應用程式或 API 使用者必須提供具有足夠長度的強式密碼。 這點很重要，因為匯入的身分識別資料包含群組的私密金鑰。

 

若要匯出目前的對等群組設定，請呼叫 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)，將控制碼傳遞給群組 (由先前的 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)、 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)或 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) 呼叫取得，以及用來加密和保護設定檔的密碼。 此函式會傳回 XML 字串，其中包含下列範例格式的設定，接著可以使用外部傳輸機制（例如電子郵件）將其寫入檔案並傳遞至另一部電腦。

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

以 XML 字串形式取得群組設定之後，您可以藉由呼叫 [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) 與設定 XML 字串以及提供給 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)的特定密碼，來匯入群組。 此函式會傳回身分識別名稱和群組對等名稱，然後將其提供給 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) ，並連接到建立的群組。

 

 



